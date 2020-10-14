---
layout: default
title: input()
---

<h2 style="color:#cb42f5">Ask players to name the 2nd planet from the sun.</h2>

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "answer = input('What is the 2nd planet? ')\n" +
    "if answer == 'Venus':\n" +
    "	print('Yes!')\n" +
    "else:\n" +
    "	print('Sorry. The planet is Venus.')\n" +
    "answer == input('What is the 2nd planet? ') #distractor\n" +
    "input('What is the 2nd planet? ') #distractor\n" +
    "if answer = 'Venus': #distractor\n" +
    "else #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


[Next](./ifelse2.html)
