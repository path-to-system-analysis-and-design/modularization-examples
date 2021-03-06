# 优化 Autonomy

为了达成 “各写各的” 的目的，在一口锅里吃饭总是要先有一些规矩的。

这部分的一致性主要靠上层业务的 stakeholder 去推动，因为独立自主是他们受益，他们是最有动力保持互相没有关系的状态。
如果各个 stakeholder 的诉求都可以独立写一个自己的页面，独立搞一个自己的流程，那皆大欢喜。
然而事情往往是大家都希望往同一个页面里加东西，都希望往同一个业务流程里夹带私货。
正是因为这些集成需求，才导致了 Autonomy 受到了挑战。
要优化 Autonomy，就要避免专职的 xxx-api 团队来集成所有人的代码，这个团队很快就会变成瓶颈。

常见的“一致性”是某种插件化架构，包括不限于微前端，OSGi，代码加载器，编译期钩子等等。
重点不在于搞出来什么，这些代码打包技术能力上都是等价的。
重点是大家都用同一套。

# 指标计算与自动检查

指标方面要特别关注“必要参数占比”。达到优化 Autonomy 的目的了就可以了，过度了就不好了。不要以一致性的名义，把不要写在一起的东西强行写一起了。如果插件小，motherboard大，motherboard天天改，那就需要反思一下了。