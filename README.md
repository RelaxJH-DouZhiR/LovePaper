# Papers on Software Engineering Interest

**Remark**：此库仅用于收集一些有趣软件工程论文的总结，全部使用LLM生成，人工修正部分已通过*斜体*标注，欢迎PR。

Main Repo: [https://github.com/RelaxJH-DouZhiR/SEPaper](https://github.com/RelaxJH-DouZhiR/SEPaper)

# Framework

推荐使用如下[框架](Framework.md)，可以根据具体论文进行修改。若添加了人工修正，请标明。

# All Papers

## Domain knowledge matters: Improving prompts with fix templates for repairing python type errors

>领域知识很重要：使用修复模板改进提示以修复Python类型错误。

[Peng, Yun, et al. "Domain knowledge matters: Improving prompts with fix templates for repairing python type errors." Proceedings of the 46th IEEE/ACM International Conference on Software Engineering. 2024.](paper/10.1145-3597503.3608139.md)

TypeFix通过挖掘修复模板并将其融入预训练模型的提示中，有效提升了Python类型错误的自动修复能力，在多个基准测试上表现优异。

---

## Exploring the potential of chatgpt in automated code refinement: An empirical study

>探索ChatGPT在自动代码优化中的潜力：一项实证研究

[Guo, Qi, et al. "Exploring the potential of chatgpt in automated code refinement: An empirical study." Proceedings of the 46th IEEE/ACM International Conference on Software Engineering. 2024.](paper/10.1145-3597503.3623306.md)

本研究首次评估了ChatGPT在代码审查任务中的表现，特别是在代码优化方面，发现其显著优于现有工具CodeReviewer，同时提出了改善其不足的策略。

---

## On Using GUI Interaction Data to Improve Text Retrieval-based Bug Localization

>关于使用GUI交互数据改进基于文本检索的缺陷定位

[Mahmud, Junayed, et al. "On Using GUI Interaction Data to Improve Text Retrieval-based Bug Localization." Proceedings of the 46th IEEE/ACM International Conference on Software Engineering. 2024.](paper/10.1145-3597503.3608139.md)

本研究通过整合GUI信息到基于文本检索的缺陷定位技术中，显著提升了面向用户应用的缺陷定位准确性，特别是在提高相关文件排名和筛选无关文件方面。

---

## ECFuzz: Effective Configuration Fuzzing for Large-Scale Systems

>ECFuzz: 针对大型系统的有效配置模糊测试

[Li, Junqiang, et al. "ECFuzz: Effective Configuration Fuzzing for Large-Scale Systems." Proceedings of the 46th IEEE/ACM International Conference on Software Engineering. 2024.](paper/10.1145-3597503.3623315.md)

ECFuzz通过多维度配置生成和单元测试验证策略，有效解决了大型系统配置测试中的组合爆炸问题，显著提升了配置引发错误的检测效率和数量。

---

## Improving Testing Behavior by Gamifying IntelliJ

> 通过对IntelliJ进行游戏化来改进测试行为

[Straubinger, et al. "Improving Testing Behavior by Gamifying IntelliJ." Proceedings of the 46th IEEE/ACM International Conference on Software Engineering. 2024.](paper/10.1145-3597503.3623339.md)

IntelliGame是IntelliJ IDE的游戏化插件，通过成就系统鼓励开发人员进行更多有效的测试，实验证明能显著提升测试质量和频率。

---

## Chain-of-thought prompting elicits reasoning in large language models

> 通过思维链提示引导大型语言模型进行推理

[Wei, Jason, et al. "Chain-of-thought prompting elicits reasoning in large language models." Advances in neural information processing systems 35 (2022): 24824-24837.](paper/Chain-of-Thought%20Prompting%20Elicits%20Reasoning%20in%20Large%20Language%20Models.md)

通过“思维链提示”方法，大型语言模型在复杂推理任务上的表现显著提升，仅需少量示例即可大幅提高解题准确率。

---

## CoderEval: A Benchmark of Pragmatic Code Generation with Generative Pre-trained Models

>CoderEval: 基于生成预训练模型的实用代码生成基准测试

[Yu, Hao, et al. "Codereval: A benchmark of pragmatic code generation with generative pre-trained models." Proceedings of the 46th IEEE/ACM International Conference on Software Engineering. 2024.](paper/10.1145-3597503.3623316.md)

CoderEval是新提出的代码生成评估基准，包含460个Python和Java任务，强调非独立函数的生成，以更真实地评估模型在实际编程场景中的表现。

---

## DistillSeq: A Framework for Safety Alignment Testing in Large Language Models using Knowledge Distillation

> DistillSeq：一种基于知识蒸馏的大型语言模型安全对齐测试框架

[Yang, Mingke, et al. "DistillSeq: A Framework for Safety Alignment Testing in Large Language Models using Knowledge Distillation." Proceedings of the 33rd ACM SIGSOFT International Symposium on Software Testing and Analysis. 2024.](paper/10.1145-3650212.3680304.md)

研究提出DistillSeq方法，通过将大型语言模型的审核知识转移到小模型，结合语法树和LLM生成恶意查询，显著提升大型语言模型的测试效率和攻击成功率，减少资源消耗。

---

## An empirical study of static analysis tools for secure code review

> 静态分析工具在安全代码审查中的实证研究

[Charoenwet, Wachiraphan, et al. "An empirical study of static analysis tools for secure code review." Proceedings of the 33rd ACM SIGSOFT International Symposium on Software Testing and Analysis. 2024.](paper/10.1145-3650212.3680313.md)

本研究评估了SAST在C/C++代码审查中的有效性，发现其可识别52%的漏洞，优先处理警告函数可提高准确性，但大多数警告与实际漏洞无关，揭示了SAST的局限性和未来改进的方向。
