---
layout: default
title: if
---

<h2 style="color:#cb42f5">Ask players the color of Mars. Print 'Yes!' if they get it right.</h2><div id="sortableTrash" class="sortable-code"></div> 

<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "answer = input(&#039;What color is the planet Mars? &#039;)\n" +
    "if answer == &#039;red&#039;:\n" +
    "	print(&#039;Yes!&#039;)\n" +
    "answer == input(&#039;What color is the planet Mars? &#039;) #distractor\n" +
    "if answer = &#039;red&#039;: #distractor\n" +
    "print(Yes!) #distractor";
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
