---
layout: default
title: While
---

<h2 style="color:#cb42f5">Make this game:</h2>
<p><ul><li style="color:#cb42f5">Repeat the following tasks...</li><li style="color:#cb42f5">Print: I'm bored</li><li style="color:#cb42f5">Ask players to press enter</li></ul></p>

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "while True:\n" +
    "	print(&quot;I&#039;m bored.&quot;)\n" +
    "    input(&quot;press enter to continue&quot;)\n" +
    "while true: #distractor\n" +
    "while True #distractor\n" +
    "print(I&#039;m bored.) #distractor";
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
