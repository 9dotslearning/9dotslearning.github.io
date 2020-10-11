---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons Practice

## Parsons 1 (Line Based Grader)
One of these blocks shows the question, "What is the most popular birth month? "
Drag and drop it into the yellow slot.

<div id="201011a-sortableTrash" class="sortable-code"></div> 
<div id="201011a-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="201011a-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="201011a-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "answer = input('What is the most popular birth month? ')\n" +
    "answer = input(What is the most popular birth month? ') #distractor\n" +
    "input('What is the most popular birth month? ') #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "201011a-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "trashId": "201011a-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#201011a-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#201011a-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


### Example Next Link
[Next](./parsons/example1.html)
