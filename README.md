# Papers on Software Engineering Interest

**Remark**：此库仅用于收集一些有趣软件工程论文的总结，全部使用LLM生成，人工修正部分已通过<u>下划线</u>标注，欢迎PR。

Main Repo: [https://github.com/RelaxJH-DouZhiR/SEPaper](https://github.com/RelaxJH-DouZhiR/SEPaper)

# Framework

推荐使用如下[框架](Framework.md)，可以根据具体论文进行修改。若添加了人工修正，请标明。

# All Papers

[Peng, Yun, et al. "Domain knowledge matters: Improving prompts with fix templates for repairing python type errors." Proceedings of the 46th IEEE/ACM International Conference on Software Engineering. 2024.](paper/10.1145-3597503.3608139.md)

作为一种动态编程语言，Python近年来变得越来越流行。尽管Python的动态类型系统方便了开发人员编写Python程序，但它也带来了运行时的类型错误，这些错误常见且不易修复。现有的基于规则的方法可以自动修复Python类型错误。这些方法能够为手动定义的模板所涵盖的类型错误生成精确的修复补丁，但它们需要领域专家设计修补合成规则，并且在实际类型错误中，模板覆盖率较低。基于学习的方法减轻了设计修补合成规则的手动工作量，并且由于深度学习的最新进展，这些方法已经变得越来越流行。在基于学习的方法中，利用代码预训练模型的知识库并通过预定义提示（prompts）的提示式方法在一般程序修复任务中取得了最先进的性能。然而，这些提示是手动定义的，并没有涉及修复Python类型错误的特定线索，导致其有效性有限。如何自动改进提示以融合领域知识来修复类型错误，是一个具有挑战性且未得到充分探索的问题。本文提出了TypeFix，一种将修复模板融合进提示式方法的新颖方法，用于修复Python类型错误。TypeFix首先通过一种新颖的分层聚类算法挖掘出通用的修复模板。所识别的修复模板表明了现有类型错误修复中的常见编辑模式和上下文。然后，TypeFix通过将通用修复模板作为领域知识，生成代码预训练模型的代码提示，其中每个类型错误的掩码位置是自适应确定的，而不是预先设定的。在两个基准测试（包括BugsInPy和TypeBugs）上的实验表明，TypeFix分别成功修复了26个和55个类型错误，分别比最好的基线方法多修复了9个和14个。此外，所提出的修复模板挖掘方法能够覆盖两个基准测试中75%的开发者补丁，比最佳的基于规则的方法PyTER提高了30%以上。

---

[Guo, Qi, et al. "Exploring the potential of chatgpt in automated code refinement: An empirical study." Proceedings of the 46th IEEE/ACM International Conference on Software Engineering. 2024.](paper/10.1145-3597503.3623306.md)

代码审查是确保软件项目质量和可维护性的重要活动。然而，它是一项耗时且常常容易出错的任务，可能对开发过程产生重大影响。最近，ChatGPT作为一种先进的语言模型，在各种自然语言处理任务中展示了令人印象深刻的性能，表明它有潜力自动化代码审查流程。然而，ChatGPT在代码审查任务中的表现仍不明确。为填补这一空白，本文进行了首个实证研究，旨在了解ChatGPT在代码审查任务中的能力，特别是基于给定代码审查的自动代码优化。为开展研究，我们选择了现有的CodeReview基准，并构建了一个高质量的新代码审查数据集。我们使用最先进的代码审查工具CodeReviewer作为基线，与ChatGPT进行比较。我们的结果显示，ChatGPT在代码优化任务中优于CodeReviewer。具体来说，ChatGPT在高质量代码审查数据集上的EM和BLEU评分分别达到22.78和76.44，而最先进的方法仅达到15.50和62.88。我们进一步分析了ChatGPT表现不佳的根本原因，并提出了几种策略来缓解这些挑战。我们的研究为ChatGPT在自动化代码审查过程中的潜力提供了见解，并指出了潜在的研究方向。

---

[Mahmud, Junayed, et al. "On Using GUI Interaction Data to Improve Text Retrieval-based Bug Localization." Proceedings of the 46th IEEE/ACM International Conference on Software Engineering. 2024.](paper/10.1145-3597503.3608139.md)

与管理缺陷报告相关的最重要任务之一是定位故障，以便能够进行修复。因此，先前的工作旨在通过将缺陷定位任务公式化为信息检索问题来实现自动化，在这一过程中，潜在有问题的文件根据与给定缺陷报告的文本相似度进行检索和排名。然而，缺陷报告中包含的信息与源代码文件中的标识符或自然语言之间通常存在显著的语义差距。对于面向用户的软件，目前存在一个尚未被深入研究的重要信息来源——图形用户界面（GUI）中的信息。在本文中，我们探讨了这样一个假设：对于面向终端用户的应用程序，将缺陷报告中的信息与GUI中的信息相联系，并利用这些信息帮助检索潜在的有问题文件，可以改进现有的基于文本检索的缺陷定位技术。为了验证这一现象，我们进行了一个全面的实证研究，使用从重现场景中获得的GUI交互信息增强四种基线文本检索技术，用于缺陷定位，以（i）筛选掉潜在的无关文件，（ii）提升潜在的相关文件，以及（iii）重新制定文本检索查询。为了开展研究，我们选择了当前最大的包含已完全定位并可重现的真实安卓应用程序缺陷的数据集，该数据集包含80个缺陷报告，来自39个热门开源应用程序。我们的结果表明，使用GUI信息增强传统技术，在多个指标上显著提高了有效性，包括Hits@10的相对提升达13-18%。此外，通过进一步分析，我们发现所研究的增强技术与现有技术在很大程度上是互补的，能够将更多的有问题文件推入前十名结果中，同时总体上保持了基线技术中的高排名文件。