---
layout: default
title: Get My Fate
---

<p style="color:#cb42f5"><ul><li>Repeat the following 3 tasks...</li><li>Create a random number from 0 to 2.</li><li>Print a message.</li><li>If the number is 0, stop repeating.</li></ul></p>
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "while True:\n" +
    "  number = randint(0,2)\n" +
    "  if number == 0:\n" +
    "    print(&#039;You got 0. Game over.&#039;)\n" +
    "    break\n" +
    "  if number == 1:\n" +
    "    print(&#039;You got 1.&#039;)\n" +
    "  if number == 2:\n" +
    "    print(&#039;You got 2.&#039;)\n" +
    "  input(&#039;press enter&#039;)\n" +
    "if number = 0: #distractor\n" +
    "number == randint(0, 2) #distractor\n" +
    "while true: #distractor\n" +
    "while True #distractor";
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
