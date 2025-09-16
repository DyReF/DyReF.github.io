<!-- <h1 align="center"> Faithful LLMs for Long-Horizon Task Planning </h1> -->

<!--
<div align='center'>
  <font size=4 color=black>ICRA 2024</font>
</div>
-->

<!--
[author1](https://www.yuque.com/zhangjiatao-grdyv/rn49ht/lq7xzy4xmxgrpgz9), [author2](https://www.yuque.com/zhangjiatao-grdyv/rn49ht/vsarazgdts43o7y4)
-->

## Abstract
Robotic planning tasks often involve diverse complexities, which make adaptive improvement through reflection particularly challenging. Existing LLM-based approaches typically rely on fixed routines, lacking the ability to adjust to task-specific complexity and often leading to redundant reflections. To address this, we propose DyRef, a dynamic reflection framework that models tasks as a Diagnostic Graph, measures tasks complexity through structural factors, and routes them through a Reflection Toolkit via a learned Routing Policy network. This design enables tailored reflection strategies that reduce redundancy and improve reasoning efficiency. Experiments in AlfWorld and on real-world robotic platforms show that DyRef improves success rates by 38.0% reducing redundant reflections by 64.4%. Project webpage (no author information) : https://DyRef.github.io/

## Video

<div align='center'>
  <video id="video" controls="" preload="none" poster="作者(图片地址)">
    <source id="mp4" src="https://github.com/Mongoosesyf/DiEP.github.io/blob/main/samll.mp4" type="video/mp4">
  </video>
</div>

## Results
Example of our frameworks for long-horizon task planning:

<div align='center'>
  <img src="https://github.com/Mongoosesyf/DiEP.github.io/blob/main/result.PNG">
</div>

## Methodology
The framework uses the task description as input and outputs the task plan. Our framework consists of three stages: 
1. Decompose a complex, long-horizon task into several simpler sub-tasks and formulate an abstract plan.
2. Represent the task goal, abstract plan, and instruction as long-term memory, while designating the selected sub-goal in the plan, demonstration, and sub-task specifics as short-term memory.
3. Input the combined long and short-term memories and the environment observation into the LLM to retrieve the sub-task plan. Update memory simultaneously and repeat the above steps until the task is complete.

<div align='center'>
  <img src="https://github.com/Mongoosesyf/DiEP.github.io/blob/main/RNN.PNG">
</div>

<br/>

<div align='center'>
  <img src="https://github.com/Mongoosesyf/DiEP.github.io/blob/main/details.PNG">
</div>

## BibTeX
