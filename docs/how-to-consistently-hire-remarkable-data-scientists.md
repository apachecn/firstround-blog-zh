# 如何持续聘用卓越的数据科学家

> 原文：<https://review.firstround.com/how-to-consistently-hire-remarkable-data-scientists>

*本文由* ***[杰里米·斯坦利](http://www.twitter.com/jeremystan "null")*******[Sailthru](http://www.sailthru.com/ "null")****的首席数据科学家兼 EVP 工程负责，他在那里负责将智能构建成公司的营销个性化平台。他的数据科学团队致力于预测、推荐和优化的算法。**

***数据科学家接受过处理不确定性的培训。不管我们处理的数据有多“大”,它仍然是一个充满潜在偏差的有限样本。我们的模型在太简单而没有意义和太复杂而不可信之间徘徊。利用控制数据中噪声的方法，我们尽可能地模拟、测试和验证一切。一个伟大的数据科学家会对他们的数据、方法和结论持健康的怀疑态度。***

*然后，有一天，一名数据科学家获得晋升，面临一个全新的挑战:评估一名候选人成为他们团队的一员。样本量下降很快，实验似乎不切实际，采访中的偏差比我们在工作中仔细控制的偏差要明显得多。*

*许多数据科学领导者诉诸于遵循传统的招聘实践——但他们不应该这样做。*

*在着手组建我的最新团队时，我与许多数据科学领导者交谈，收集他们的想法和最佳实践。我尤其受到了 **[赖利·纽曼](https://www.linkedin.com/in/rileynewman "null")** 的想法的影响， [Airbnb](www.airbnb.com "null") 的数据科学主管，他[设计并实施了](http://www.quora.com/How-does-Airbnb-hire-data-scientists "null")一种完全不同的招聘数据科学人才的方式，我在设计这个系统时与他交谈过几次，我将在这里与你分享。我还从佛罗里达州[项目](http://projectfla.com/ "null")的 **[德鲁·康威](http://drewconway.com/ "null")** 那里学到了很多东西，他不断改进他的招聘流程，以选择能够正好落在他著名的[数据科学维恩图](http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram "null")中间的人才:*

*![](img/7c30bc0cc71a22f521f137018fce7771.png)*

*在本文中，我将概述 Riley 开发并根据这项研究进行调整的新流程的目标，描述其基本原则，并介绍我们在 Sailthru 进行实验的实现。当然，如果不展望进一步适应和改进流程的机会，本指南将是不完整的。*

# *如何开始一场招聘革命*

*在发展我们的招聘流程时，我们着手改进以下可衡量的目标:*

***准确性**:最大化新员工成为优秀员工的机会。*

***损失**:尽量减少优秀人才提前离开招聘渠道的可能性。*

*成功:最大化工作机会被接受。*

***努力**:尽量减少对招聘团队的长期干扰。*

*乍一看，任何有经验的经理都会认为不可能同时提高上述四个目标。前三者在实践中往往相互矛盾(例如，候选人越优秀，就越难让他们接受聘用)。除此之外，改进它们似乎要求团队付出更大的努力。*

*在传统的招聘过程中，如果准确率高达 50%，大多数经理都会感到幸运。也就是说，不超过一半的雇员是优秀的。损失是很难衡量的(毕竟，过程中掉队的候选人不是来为你工作的)，大多数经理担心他们会定期失去惊人的人才，因为他们的过程是如此漫长和繁琐。*

*在数据科学这种竞争激烈的领域，实力强的候选人往往会收到 3 个甚至更多的 offers，所以成功率一般在 50%以下。*

*招聘所需的持续工作很容易消耗数据科学团队 20%或更多的时间。*

*在与其他数据科学领导者验证了这一经验后，我试图实施一个可以实现以下目标的流程:*

***准确性**:事实上，90%的雇员应该是优秀的员工。*

*损失:我们应该向进入我们漏斗的 80%的优秀候选人发出邀请。*

***成功**:应接受 65%的延期报价。*

***努力**:招聘应该消耗团队不到 10%的时间。*

*通过设计一个更聪明的招聘流程——既能发现优秀的候选人，同时又能降低失去他们的风险——就有可能同时实现前三个目标。此外，通过前期大量投资(这种投资随着时间的推移会获得丰厚的回报)，可以管理团队的持续努力和分心。*

***为了确保实现我们的目标，我们制定了一套适用于任何职位招聘的核心原则**。让每个人保持专注和一致的原则可以极大地帮助任何大的过程改变。当您迭代这个过程时，它们也是一个健康的基础。他们在这里:*

****确保你的招聘过程持续进行并不断改进*** 。*

*人们通常认为招聘要么是你偶尔参与的一项任务，要么是周期性的全力以赴的闪电战。相反，把你的招聘流程设计成一个永远运转的引擎，一个可预测的人才漏斗在清晰的阶段流动。这确保了你总是在招聘，无论何时优秀人才来到市场，你都有机会参与进来。*

*投资于一个永远在线的过程会迫使你把招聘当成一门学科。这将推动协议和结果的一致性，使您能够收集关于成功和失败的数据，并迫使您以管理数据管道的同样谨慎管理您的人才管道。*

*让你的过程反映你招聘需求的现实。*

*残酷的事实:标准的面试问题有致命的缺陷。*

*询问求职者以前的经历，你会发现他们是否能清楚地说出在其他工作中发生的事情。问他们一些技术问题，你会发现他们反刍知识的能力。让他们在白板上解决一个“玩具”问题，你会发现他们解决玩具问题有多快。成功通过所有这些障碍的候选人在实践中可能是一个完全无效的数据科学家。*

*为了解决这些缺陷，你必须首先非常清楚地了解你希望候选人如何执行数据科学。在最高层次上，您应该清楚您的团队将生产的最终产品。是可视化和分析为决策者提供信息吗？给开发者的设计和原型？或者可以在生产环境中扩展和支持的应用程序？*

*接下来，你要清楚的知道你希望成功的候选人做什么。确定您希望看到数据科学家抓住的五个机会。对于每一个，确保你有(或者可以合理地收集)所需的数据，并且可以设想一个有效的解决方案，即使你自己不能设计它。这些机会存在于贵公司的近期战略、贵公司或产品如何运作的可行性以及贵公司目前拥有或能够合理生成的数据的约束条件之间。*

*知道你的团队如何执行数据科学的答案，以及你最希望候选人能够应对的挑战，你就可以设计一个紧密反映你工作条件的招聘流程。这意味着你应该把候选人放在一个与他们的“日常生活”非常相似的环境中。如果他们能在面试过程中在那种环境下成功，那么他们长期成功的机会就大得多。*

*首先进行客观的评估，以减少你的偏见。*

*那些表现优异的候选人可能会在传统的面试过程中失败。*

*罪魁祸首是面试官的偏见。当你和候选人一起走进房间时，你就开始对他们的能力形成看法(大多是无意识的)。这种偏见有很多种([查看这里的 100 多种认知偏见列表](http://en.wikipedia.org/wiki/List_of_cognitive_biases "null"))，但面试中最常见的偏见是偏爱与自己相似的人。*

*伟大的数据科学家必须具备非常强的定量和编程技能。这没得商量。因此，我们设计了我们的流程，首先测试这些技能，然后转移到更主观(但仍可测量)的技能，如解决问题和沟通。只有在最后，我们才能了解最主观的部分——候选人如何在团队中工作，如何融入文化。*

*这些后期的、更主观的标准是最费时的评估，也是偏见最容易滋生的地方。将他们移至漏斗的后期有两个好处，一是减轻团队的负担(在我们确信他们拥有我们需要的技能之前，我们不会评估文化契合度)，二是最小化过早失去优秀候选人的风险。*

****设计你的流程去推销候选人。****

*大多数面试过程也没能推销出最优秀的候选人。面试往好里说是压力重重，往坏里说是平淡乏味。候选人经常被迫向 4 个或更多的面试官重复他们的故事，并连续几个小时回答问题。之后，虽然他们可能会问一些自己的问题，但他们常常难以想象在这家公司工作会是什么样子。然后，他们等了几天才收到很少诚实或及时的反馈。那么，如何修复如此破损的东西呢？*

*创建一个流程，向候选人提供数据和问题，反映他们将在您的组织中面临的真正挑战。最重要的是，确保你的招聘过程能让应聘者感受到你团队的活力和文化，这样他们才能真正体会到和你一起工作的感觉。每个候选人都应该带着对加入你的团队的信任来完成面试过程。*

****和你的团队一起做出明智的决定，而不是在你的塔里。****

*无论你如何招聘，每个经理都必须做出艰难的决定。要自信地做出决定，在你的漏斗的每个阶段建立清晰的评估候选人的框架。这包括定义团队中每个人都理解的目标和指标。*

*此外，作为一个团队公开做决定。这可以确保招聘经理从参与招聘过程的每个人那里听到关于候选人的直接反馈。更重要的是，它确保你们都在寻找相同的品质。一个开放的论坛有助于随着时间的推移改变你的招聘需求和策略。*

*最后，让你的跨职能合作伙伴参与评估你的候选人。数据科学永远不会真正在真空中完成。你将与决策者、工程师和产品经理合作。让这些领域的关键合作伙伴参与进来，这样您就可以挑选出能够在各个部门取得成功的人才。*

****行动比市场快。****

*优秀数据科学人才的市场竞争异常激烈，因此您的流程应确保尽快让候选人通过您的漏斗，保持良好的势头，并最大限度地降低他们接受竞争性报价的机会。快速行动需要一个简化的过程，让你建立自信和速度。投资工具和物流来跟踪候选人在你的漏斗的每个阶段停留多长时间，并积极改变你的系统以获得保持你的优势。*

# *实施游戏*

*在电影 *[模仿游戏](http://www.imdb.com/title/tt2084970/ "null")* 中，艾伦·图灵的管理技巧差点让英国反情报部门破解德国恩尼格玛加密机的努力脱轨。当他意识到他需要帮助时，他已经疏远了布莱奇利公园的团队。然而，在这位著名的计算机科学家**灵光一现的时候，图灵发明了一种完全不同的方法来招募新的团队成员。***

*为了组建他的团队，图灵开始寻找新的人才，他在伦敦《每日电讯报》上发表了一个纵横字谜，邀请任何能在 12 分钟内完成这个谜题的人申请一个神秘的职位。成功的候选人被召集在一个房间里，进行一次定时测试，在一个受控的环境中挑战他们的数学和解决问题的技能。在测试结束时，图灵向大约 30 名候选人中表现最好的两人发出了邀请。*

*从这件轶事中可以学到很多东西。*

*这一过程确保了图灵尽可能广泛地网罗可用人才，用一个具有挑战性的问题和诱人的就业机会吸引他们，然后在一个受控的环境中验证他们的技能。在电影中的一个虚构的事件转折中，图灵招募的候选人之一是一个名叫琼·克拉克的女人，她成为了一个非常亲密的合作者。琼非常有才华，但考虑到当时的偏见，如果不是因为图灵的科学招聘方法，她几乎肯定会被忽略，无法成为一个破译代码团队的成员。*

*就像模仿游戏中的*一样，我们让候选人经历一系列近似其潜在工作环境的经历，并评估他们解决问题的技能，一旦我们雇用他们，这些技能高度预示着他们的成功。令人惊讶的是，通过正确的规划和前期投资，这可以比传统面试更有效地完成，并节省团队的时间。**

*最高级别的面试流程有两个关键部分:*

***带回家的测试:**测试考生解决一系列越来越难的挑战的能力的简短练习。*

***数据日:**花一整天时间与团队一起完成一个更加开放的挑战，最后向一组人展示他们的工作。*

*我们将这一过程作为一个漏斗来管理。在 500 名入境申请者中，250 人(50%)将提交一份带回家的测试，25 人(10%)将通过，20 人(80%)将参加数据日，4 人(20%)将通过数据日，然后 3 人(75%)将接受聘用。这意味着为了找到一个优秀的雇员，我们需要超过 150 个申请人。*

*这里要用到的关键杠杆是 **(A)** 漏斗中申请人的质量， **(B)** 提交带回家测试和参加数据日的成功率，以及 **(C)** 带回家测试和数据日过滤器的准确性。通过这个漏斗跟踪你的候选人，并按渠道检查每个阶段的损失(例如，他们来自哪里)，你可以开始识别表现更好的渠道，以及你的漏斗中过滤过于积极的阶段。*

*考虑到我们的四个不同目标——最大化*准确性*(雇佣优秀员工)和*成功*(确保他们接受聘用)，同时最小化*损失*(候选人提前放弃)和*努力*(团队分心)——我们投入了大量时间来设计一个清晰高效的流程，该流程由数据驱动，对候选人有吸引力。*

***这个过程有以下六个阶段，从最简单、最客观到最困难、最主观:***

***预筛选**:检查脉冲*

*带回家的测试:测试足够的技能*

***推销**:说服他们参加“数据日”*

***数据日**:在真实、可控的环境中测试能力，评估文化*

*决定:做出一个快速而明确的决定*

***沟通**:跟进每个候选数据日*

*让我们从战术的角度更深入地了解一下每个阶段。*

***1。预筛选***

*请注意，在 Sailthru，我们根本不会预先筛选数据科学候选人。我们不必审查他们的简历或争论他们的经验或资格。*

*如果他们有脉搏(和电子邮件地址)，我们会给他们带回家测试。*

*这是我们版本的*模仿游戏*填字游戏。这可以节省大量的时间和精力，让你更快地与有前途的候选人接触。*

*但不进行预筛选的最重要原因是，它消除了初始偏差的一个巨大来源。许多非常有才华的候选人不具备招聘人员所要求的教育或经验。这不仅意味着你失去了优秀的候选人，而且你还将激烈地争夺那些在理论上看起来不错的候选人——其他人也想要他们。*

***2。带回家测试***

*课后测试非常重要。这是筛选候选人的第一道防线，考虑到潜在的提交量，需要你的团队做最多的工作。这也是候选人第一次感受到你的团队在做什么。这个阶段不仅是防止你在不合格的候选人身上浪费时间的关键一关，也是向候选人推销角色的极其重要的一环。出于所有这些原因，当你通过漏斗收集关于候选人表现和兴趣的数据时，你应该不断发展你过程的这个阶段。*

***声音带回家测试应具有以下属性:***

***不言自明的** -你希望尽量减少候选人有问题或需要澄清的机会。*

***有界** -对于一个熟练的候选人来说，应该不超过 2 个小时就可以完成。*

***脱敏**——它会被广泛分发，所以不要包含任何专有或敏感数据。*

***相关**——将问题与你在工作中实际面临的最大挑战对应起来。*

*直接——明确你希望如何回答测试，以及你将如何评估候选人的表现。*

***分级**——问越来越难的问题，这样你就可以很容易地判断出应聘者的真实技能水平。*

*要设计您的带回家的测试，首先从您希望现有数据科学团队解决的最紧迫的问题开始。在这些问题中，挑选一两个你 **(A)** 拥有或者可以编造出令人信服的数据的问题， **(B)** 解决起来会很有趣，而 **(C)** 可以简化(也许是粗略地)成一个非常强的候选人可以在两个小时内解决的问题。*

*在你浏览了问题空间之后，编辑需要的数据来回答你的带回家的问题。理想情况下，这些数据来自您的生产环境，经过充分的清理、置换或聚合，即使落入任何人手中也不会造成伤害(假设最终会这样)。*

*或者，您可以构建完全虚假的数据，但要小心，因为数据科学中的许多挑战来自于处理不一致和异常值。我建议提供大约 100 万行数据(可能还有多个文件)，这足以在不增加负担的情况下关注所用代码的性能。*

*一旦你收集了数据，构思 2-3 个非常清晰的问题，这些问题的难度逐渐增加，并有明确的、可衡量的答案。确保你的问题不仅能测试候选人处理数据的能力，还能测试他们对分析进行逻辑思考的能力，以及从任何模型中解读结果的能力。*

*根据收集的数据和选择的问题，起草说明。这应该是一个简短、易读的文档，描述所提供的数据并包含最终问题。此外，你应该指导候选人应该使用多少时间，不是强迫他们限制他们的时间，而是指出你估计需要多少时间，这样他们就不会花几天时间在一个应该花几个小时的任务上。*

*最重要的是，包括一个你希望候选人如何回答问题的部分。你希望他们使用什么工具？您希望他们如何提交答案？就代码质量而言，你在寻找什么？可视化或解释对你来说重要吗？小心你在这里要求的东西。这是你推销自己和公司的一个重要机会。*

*接下来，将带回家的测试交给你的其他团队成员或社区中的朋友。用这个来校准测试，确保你对最终答案有共识。你最不希望的就是候选人纠结于模棱两可。*

***最后，建立评估提交材料的清晰框架。考虑这些标准:***

***正确性**——他们得到正确的最终答案了吗？*

***逻辑**——他们的回答听起来有逻辑吗？*

***假设**——他们有没有明确任何假设？*

*代码质量 -代码是可执行的、经过测试的、有效的、有文档记录的吗？*

***效率**——代码是否简洁且性能合理？*

***使用的技术**——他们是否恰当地使用了现代工具和库？*

***沟通** -答案是否清晰，并以合理的方式呈现？*

***3。销售宣传***

*一旦候选人通过了你的课后测试，你的下一个挑战就是说服他们来参加你的“数据日”面试。大多数人会期待一个传统的面试，他们在你办公室呆的时间不超过 4 个小时——当然不是一整天。你必须让他们相信这是值得的。*

*你的推销的关键部分是你如何与候选人联系，你如何清楚地表达你正在展示的令人兴奋的机会，以及你如何为数据日描述和准备他们。这一切都应该有助于培养他们的兴趣和热情— **现在不是你评估他们的时候**。*

*每个候选人都有不同的动机，所以你必须认真倾听，将谈话引向他们最关心的话题。根据我的经验，我发现以下是关键的激励因素:*

*产品和公司的整体潜力。*

*数据科学是如何组织的，它在哪里报告，以及它迄今为止产生了什么影响。*

*数据科学在不久的将来将面临的主要挑战或机遇。*

*数据科学如何与其他团队跨职能合作。*

*现有数据的范围、规模和质量，以及未来收集的机会。*

*团队如何管理他们的工作，如何在优先级和决策方面进行协作。*

*团队使用的特定工具和技术。*

*最终，你会发现候选人不能或不愿意安排一个数据日。最终，虽然这可能意味着你会错失良机，但你必须愿意冒这个险。*

*【数据日】成为你评估所有候选人的黄金标准。*

***4。数据日***

*从很多方面来说，数据日本身就是招聘过程的核心。做得好的话，它包含了对候选人的最终技术、战略和技能评估，以及对他/她的文化契合度的分析，这种体验真正地在你的团队和公司中“推销”了他们。有了足够的准备，你或你的团队不需要投入比传统面试更多的时间就可以完成。*

*准备工作清单包括:*

***说明**:一份简明扼要的文件，描述了当天的挑战、数据和评估标准，以及候选人成功所需了解的一切。*

***数据**:丰富的生产数据摘录，将挑战和激励你的候选人。一个伟大的数据科学家应该能够花一周的时间研究这些数据而不会感到厌烦。*

***笔记本电脑**:一款全新的功能强大的笔记本电脑，与他们工作时使用的电脑完全相同，预装了他们需要的所有数据和应用程序。*

*准备对于成功的数据日至关重要。通过确保候选人拥有高效工作所需的一切，你可以最大限度地利用他们完成有意义工作的时间。*

**指令**

*当候选人到达他们的数据日时，你首先应该提供一套打印的说明。要考虑包括(尽可能简明)的部分有:*

*简介-对一天的日程和任务的快速欢迎和介绍。*

*免责声明(可能是 NDA) -咨询您的法律部门是否需要免责声明。*

*目标——手头任务的高层次概述，以及你在一个成功的数据日里的期望。*

*建议的时间表——你认为候选人会如何利用他们的时间。明确表示他们将面临的最大挑战是时间不够了。*

*数据——对您提供的数据的广泛描述，足以为下面的部分提供上下文。*

*主题——一个 4 或 5 个可以考虑的主题的简明列表(稍后将详细介绍如何选择这些主题)。*

*评估——你想从成功的候选人身上得到什么。*

*技术设置-笔记本电脑上提供的工具的简要说明。*

*数据细节-对所提供数据的更全面的描述。对于每个文件，描述整体内容、包含的每个字段以及数据集中的大小(行数或观测值数)。*

*最重要的是选题。这些应该足够多样化，让不同背景的候选人都能找到他们感兴趣且平易近人的东西。同时，确保将话题集中在对你的业务有价值的应用上。这确保了你在测试你需要的技能，并让候选人对他们在你的团队中会做什么有一个更现实的感觉。*

*最后，主题应该作为建议提出。我更喜欢让候选人在这里自由支配。最后，最重要的是，他们有信心在一天结束前做出有意义的分析和演示。*

*请记住，如果你的指示清晰且切中要点，你回答候选人问题的时间会少得多。*

**数据**

*接下来要考虑的是候选人将使用的数据。这个数据集应该在两个方面不同于带回家的数据集。第一，它不会被广泛分发，所以你应该绝对使用生产数据。但是请记住，虽然候选人将使用您提供的笔记本电脑，但他们将连接到互联网，因此您不能保证完全控制数据集。因此，确保不包含个人身份或具有战略重要性的数据。*

*第二，这个数据集应该大而丰富。您可以包含更多的观察结果、多组数据、复杂的时间序列以及关于每个观察结果的各种数据点。数据日的关键挑战之一是要求候选人获取一组“真实世界”的数据，并确定一个实用的分析或建模路径。这通常需要忽略大量的可用数据，或者通过过滤或聚合来显著简化数据。*

*最后，最强的候选人如何使用你提供的东西会让你大吃一惊。*

*一个重要的考虑因素是您应该提前对数据进行多少预处理。一般来说，除非您特别想测试他们清理非常混乱的数据的能力，否则我建议保持这个样本相当干净，以确保他们不会在 munging 上浪费宝贵的时间，否则这些时间将用于分析或建模。*

**笔记本电脑**

*向候选人提供一台笔记本电脑，将说明、数据和软件都放在一个容易拿到的地方。在 Sailthru，我们使用 MacBook Pro(所有数据科学家和工程师都使用 Mac 或 Linux 机器)，我们安装以下软件:*

*[自制](http://brew.sh/ "null")*

*[蟒蛇](https://store.continuum.io/cshop/anaconda/ "null") (Python 发行版)*

*[R](http://www.r-project.org/ "null")*

*[RStudio](http://www.rstudio.com/ "null")*

*[Emacs](https://www.gnu.org/software/emacs/ "null") 和 [Vim](http://www.vim.org/ "null")*

*[Java 7](https://www.java.com/en/download/faq/java_7.xml "null")*

*[日食](https://eclipse.org/ "null")*

*借助自制软件，数据科学家可以根据需要快速安装其他软件。此外，我们将数据放在主目录中的 CSV 文件中。我们建议考生使用开源脚本语言(如 Python、 [R](http://www.r-project.org/ "null") 或 [Julia](http://julialang.org "null") )提交他们的课后测试，这样每个人都会感到舒服。*

**日程**

*Sailthru 典型数据日的时间表如下所示:*

*上午 10 点——欢迎应聘者到达后，受到招聘人员的欢迎，并被带到团队旁边的指定位置。*

***上午 10:05-伙伴**候选人的伙伴(我们数据科学团队的指定成员)带候选人去喝咖啡，并带她或他参观办公室。*

***上午 10:15——入职培训**这位朋友给求职者当天的指示，以及面试笔记本电脑和在哪里可以找到数据的简要说明。*

***上午 10:20-方向**候选人坐下来阅读说明并检查数据，通常会决定一个追求的方向。*

***上午 11:30-起立**候选人收听每日团队起立会议，以了解他或她将从事的工作，并被要求就他或她所追求的方向发表讲话。*

***下午 12:30-午餐**几个团队成员带候选人出去吃午餐，进一步了解他/她的背景和个性，并让候选人提出任何问题。*

***根据需要提问**候选人可以向团队中的任何人提问数据、技术或背景问题，但如果可能的话，通常会从他们的“伙伴”开始。*

*下午 4:30-提醒我们提醒候选人，他/她将在 5:30 做演示，并鼓励他们开始做演示。*

*下午 5:30-陈述候选人陈述 20 分钟他/她一天的发现或创造，然后是 10 分钟与团队和其他与会者的丰富问答。*

*下午 6 点——反馈我们要求候选人就他/她的经历给我们反馈。然后，这位朋友或招聘人员将候选人领出来，并设定我们何时传达决定的预期。*

*下午 6:15——决策团队结束了对候选人的讨论，90%的情况下已经做出了决定。*

*总的来说，团队投入的时间非常合理。这位朋友早上花 15 分钟，下午再花 15 分钟回答问题。不管怎样，起立鼓掌和午餐还是要进行的。五人一组的演示和问答需要 30 分钟，然后通常再花 15 分钟做决定。总的来说，团队花在候选人身上的时间刚刚超过 4 个人小时，不超过极简主义传统面试的时间。*

*从文化契合度的角度来看，迄今为止一天中最有见地的部分是午餐，在这里你可以看到候选人在非正式的社交场合是如何表现的。*

*从技术角度来看，一天中最有见地的部分是演讲后的问答，我们试图提出探索性和挑战性的问题，以验证候选人方法的严谨性，并确定他们如何参与我们团队中常见的热烈的技术或分析辩论。*

**吸取的经验教训**

*数据日应该是你的团队和公司的反映，所以你应该调整这个过程以适应你的具体需求。我们会在一天结束时询问候选人的反馈意见，并且已经根据他们的意见做出了许多改变。以下是我们学到的一些最好的经验:*

***考生几乎总是用完时间**。鼓励他们选择一个他们有信心的方向，并对他们的工作采取迭代的方法。这样，如果他们的方法不太好，他们有足够的时间去适应。此外，强调一个不确定的分析要比一个含糊不清的结论好得多。*

***不要让午餐时间太长**。候选人的工作时间是有限的，45 分钟后，他们将开始担心如何及时完成演示。*

*邀请不同的团队参加演示。任何你认为候选人会经常接触的人都应该在场。这让你有机会征求他们对个人工作和沟通方式的反馈，并让你的候选人更好地了解关键的内部关系。*

***在候选人到来之前，要让他们清楚数据日需要什么。这样他们就有时间为这次经历做好心理准备，从而减轻一天的压力。***

***5。决定***

*在 Sailthru，我们根据以下维度评估候选人:*

***1。问题构建**你是如何构建问题的，你做了哪些假设，你是如何缩小范围的？*

***2。技术严谨性**你为完成工作而开发的代码的可靠性、可读性和灵活性如何？这种方法的可扩展性如何？*

***3。分析的严谨性**您所应用的方法(机器学习、统计、分析、可视化)在逻辑上有多合理、完整和有意义？*

***4。沟通**您对自己的工作、方法、手段和结论的描述有多清晰？你回答问题的效率如何？*

***5。如果有生产价值，你的工作成果对 Sailthru 有多大用处？***

*我们在数据日说明中包含了这些标准，以便候选人知道成功是什么样子的。*

*候选人完成陈述和问答后，他们的朋友会带他们离开办公室。然后我们立即开始讨论候选人，趁每个人的印象都还新鲜。我们给每位参与者一个机会分享对上述标准的反馈(如果他们有意见)，首先从我们团队以外的人开始。然后我们团队中最没有经验的成员发言，接着是最有经验的成员。这有助于防止团队或领导提前偏向房间里其他人的意见。*

*一般来说，如果任何一个参与者对候选人强烈‘否定’，这就足以成为拒绝他们的理由。*

*由于技术原因，这种情况很少发生(带回家的测试应该证明大多数候选人具有合理的生产力)。但当它发生时，你应该仔细重新评估你的测试，以确保它有效地筛选候选人。*

*当这是因为文化契合或沟通原因而发生时，公开讨论这个问题是至关重要的。这有助于建立和加强你的团队想要如何表现的健康规范，并减少屈从于个人偏见的风险。*

*如果每个人都对候选人不冷不热，这也是一个明显的“不”。这通常是由于他们工作的局限性——他们完成了多少，他们思维的严谨性，或者他们的技术执行。如果僵局仍然存在，那么要么团队领导应该做出最终决定(宁可拒绝)，要么在极少数情况下，你可能想邀请候选人回来进一步讨论。*

***6。通信***

*这一过程的最后阶段是向候选人传达结果。那些没有通过带回家测试的人会收到我们招聘人员的回复。我们很乐意给每一个提交直接的反馈，但考虑到我们审查的提交数量的规模，这是不切实际的。*

*也就是说，数据科学团队的一名成员会跟踪每个在数据日到来后没有收到录用通知的候选人。这确保这些候选人收到建设性的反馈，并能从经验中学到更多。*

*最终，我们对每个数据日候选人的潜力感到兴奋，并希望既尊重他们的时间，又保持联系，以防我们再次相遇。数据科学是一个小社区。*

*![](img/975f7fd5f84f2458eb02610397d60385.png)

Before joining Sailthru, Jeremy Stanley served as CTO at Collective and Director of Global Markets Analytics for Ernst & Young.* 

# *挑战和未来机遇*

*雇用优秀的数据科学家很困难，虽然我相信这一过程对我们在 Sailthru 的招聘产生了巨大的积极影响，但我也相信我们还有很多要学习的。这是我们继续努力的方向。*

***最小化假阴性***

*我们的流程可能会产生太多的误判，例如，非常适合数据科学的候选人没有收到录用通知。最大的来源可能发生在带回家测试阶段，在这个阶段，考生可能不愿意投入时间来完成测试。让有才华的候选人更容易完成考试，并提高我们组织在社区中的品牌，这都是我们可以采取的措施。最终，这是一个管道开发的问题，并且是有问题的，因为它降低了你雇佣最优秀人才的能力。*

***放弃在数据日苦苦挣扎的优秀候选人更令人担忧，因为这些候选人投资了我们，我们也投资了他们**。发生这种情况有几个原因，但最常见的是数据日是一个高压环境。候选人必须在 8 个小时的时间里学习一个新的数据集，构思一个问题，开发一个解决方案，并制作一个演示文稿。*

*虽然一些候选人在这种压力下表现出色，但其他人变得不知所措，无法向我们展示他们通常能够完成的事情。不幸的是，我们无法在决策中考虑这一点，因为这几乎不可能与无能或低效区分开来，而这两者都是我们极力反对的。*

*候选人在数据日可能不成功的另一个原因是他们不熟悉工具。他们可能对专有或商业工具，或其他操作系统有更多的经验。这可以通过获得更多商业软件的许可和在虚拟机上提供 Windows 的使用来缓解。这些选择伴随着巨大的现金和运营成本。此外，熟悉 Linux 操作环境和开源工具是我们强烈要求的。**入门***

*可以说，这一过程中最具挑战性的方面之一是启动并运行它。如果没有一个可靠的团队来适应、执行和优化这一流程，许多组织将会为此而挣扎。*

*此外，该系统需要数据科学团队和招聘团队之间的协作。两者都必须确信它值得投资和继续发展，否则随着时间的推移，它将不可能很好地实现和维护。*

***为其他功能定制该流程***

*在 Sailthru，我们正在积极地为其他部门，如软件开发部门，塑造这个过程。该流程的结构可以基本保持不变，但所面临的具体挑战可能会有所不同。*

*例如，对于开发人员，您可以提供一个干净的 Github repo，并要求他们构建一个简单的应用程序，给出明确的需求和验收标准。这提供了一个机会，不仅可以看到他们如何设计和编写应用程序，还可以看到他们如何开发他们的软件(例如，测试驱动的开发)以及他们如何记录他们的实现。*

*或者，您可以从现有的应用程序中提取一部分，将其简化为开发人员可以轻松运行的内容，删除某个特定的功能，然后让他们重新编写代码。这使您可以看到它们是如何与您现有的代码一起工作的，并且您已经对该特性应该如何实现有了一个清晰的基准。*

# *外卖*

*对于我领导的数据科学团队来说，这一招聘流程确实是革命性的。我们已经错过了那些在论文和谈话中看起来很完美的候选人，但是他们不能构建开放式数据问题或者为他们的分析选择辩护。*

*我们聘用了以前可能从未聘用过的候选人。*

*例如，在过去，我筛选掉了几乎所有没有几年工作经验的候选人，因为我担心他们会过于注重学术。但是使用这个过程，我们雇佣了一个数据科学家，他只有一个定量的博士学位和一些实习经历，因为他在数据日展示了杰出的实践技能。他在头两周开始推动生产变革，并在头三个月产生了巨大的积极影响。*

*然而，这个过程中我最看重的是，它从我们的决策中消除了大量的怀疑和不确定性。**招聘是我们作为经理做出的最重要的决定之一**，在有明确证据支持的情况下满怀信心地做出这些决定，感觉棒极了。*

*当我们发现一个有前途的候选人时，我们可以迅速行动，因为我们知道我们已经在我们的组织和团队中推销了这个候选人，并且已经做好了在激烈的招聘市场中获胜的准备。另一个额外的好处是，我们能够雇用许多人，他们继续为公司做出巨大的贡献，而不是总是争夺每个人都认为在纸上看起来最好的候选人。*

*投入时间和精力来建立一个持续的过程，这个过程可以快速而确定地进行，并选择那些擅长应对你的真正挑战和机遇的候选人。*

*那就不要担心招聘问题，回去做伟大的数据科学吧。*