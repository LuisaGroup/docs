# 简介
## 什么是LuisaCompute
LuisaCompute(简称LC)是一个跨平台(Linux，Windows, MacOS)，多计算后端(CUDA, DirectX-12, Metal)，多语言前端(C++, Python, Rust)的高性能并行计算框架。其入门门槛低，开发方式简单，可广泛应用于离线/实时渲染器，物理模拟等领域。

## 为什么要使用LC
无论是在工业界还是在研究领域，硬件的进步使得使用现代流处理器进行高质量并行计算成为可能。然而，图形API是碎片化的，现有的着色语言缺乏多态性等高级结构，这增加了开发和维护跨平台高性能计算程序的复杂性，成本和学习门槛。这套解决方案的设计，意在解决上述的问题，Luisa一词意为Layered and Unified Interfaces on Stream Architectures，即层级化的，统一的，针对流处理器架构所设计的计算接口。在计算代码的编写方面，采用DSL(领域特定语言)+ 代码生成的方式，在原生语言上实现了一层表达力更强，更加动态的语言前端，这让用户不再需要通过原始的预编译宏，而是使用更高级的元编程控制自己的编译流程。同时运行时(runtime)的调度管线，也会对提交的任务进行动态调度优化，这通常比人工编写的调度方法方便，且效率更高，同时这套运行时系统与DSL语言前端紧密结合，让用户更少的为可能的大意浪费时间或为琐碎的优化问题烦恼，更容易写出优雅且高效的解决方案。

## 与业界其他方案的区别
在开始使用LC之前，请了解其与其他相似方案的区别，以便于您区分和根据自己的需求决定要使用的方案。

### 与Pytorch, TensorFlow的区别
Pytorch, TensorFlow等框架，常用于机器学习等需要高维矩阵计算的领域，在这方面LC暂未计划在传统GPU开发基础上提供更多相关的扩展，因而并不适合这类相对特种的需求，由于更贴近底层，其更适合传统GPU工作的离散类计算领域，如图形学计算等。

### 与Taichi的区别
作为同为提供Python前端接口的通用计算框架，Taichi以科研，实验，学术用途为主，社区更活跃丰富，更注重易用性；而LC在理念上更偏向工程性，设计目标优先考虑更高性能的硬件表现，两者虽貌似，且LC在开发时对Taichi的许多设计多有借鉴，但两者在理念上有较大区别，需用户根据需求谨慎斟酌。

## 谁在使用LC
如果您在使用LC，欢迎点击编辑[此页面](https://github.com/LuisaGroup/LuisaComputeDoc/blob/main/zh-cn/about/introduction.md)通过PR将信息提交至下面的列表，让更多的用户了解有多少用户在使用LC，也能让用户更加安心使用LC。
我们也会有更多的动力去持续投入，让LC项目和社区更加繁荣。
<table>
  <tr>
    <th>用户 (公司名/个人联系方式)</th>
    <th>项目 (项目简介/项目地址)</th>
    <th>评论 (可选)</th>
  </tr>
  <tr>
    <td><a href="https://github.com/LuisaGroup">LuisaGroup</a></td>
    <td><a href="https://github.com/LuisaGroup/LuisaRender">LuisaRender</a></td>
    <td>于SIGGRAPH Asia 2022发表文章<a href="https://luisa-render.com/">LuisaRender: A High-Performance Rendering Framework with Layered and Unified Interfaces on Stream Architectures</a></td>
  </tr>
</table>

## 联系我们
* Email: zsk20@mails.tsinghua.edu.cn maxwellgeng@outlook.com