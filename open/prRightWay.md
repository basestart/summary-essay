### 如何(正确)提交代码

> 你已经找到了一个你喜欢的项目，你已经准备好做出贡献了, 以下是如何以正确的方式获得你的贡献。

##### 有效地沟通

无论您是一次性的贡献者还是尝试加入社区，与他人合作是您在开放源代码中开发的最重要的技能之一。

> (作为一名新贡献者)我很快意识到，如果我想要结束这个问题，我就必须提出问题。我浏览了一下代码库。一旦我对发生了什么有了一些了解，我就要求更多的方向。瞧!在得到了我需要的所有相关细节之后，我终于解决了这个问题。 — @shubheksha, A Beginner’s Very Bumpy Journey Through The World of Open Source

在提问或者发起pull request时，或者在聊天中问一个问题之前，记住这些要点，以帮助有效地实现你的想法。

给问题的场景。帮助别人快速理解。如果您遇到错误，请说明您正在尝试做什么，以及如何重现错误。如果你在提出一个新想法，解释一下为什么你认为它对项目有用(不仅仅对你有用!)

```
  “X doesn’t happen when I do Y”

  “X is broken! Please fix it.”
```

事先做好功课。不了解不要紧，但要表现出你的努力。在寻求帮助之前，一定要检查项目的自述文件、文档、问题(打开或关闭)、邮件列表，并在互联网上搜索答案。当你表现出你在努力学习时，别人会欣赏你。

```
  “I’m not sure how to implement X. I checked the help docs and didn’t find any mentions.”

  “How do I X?”
```

保持请求的简短和直接。就像发电子邮件一样，每一个贡献，无论多么简单或有用，都需要别人的review。许多项目收到的请求比可以提供帮助的人要多。保持简洁。你将增加有人帮助你的机会。

```
  “I’d like to write an API tutorial.”

  “I was driving down the highway the other day and stopped for gas, and then I
   had this amazing idea for something we should be doing, but before I explain
    that, let me show you…“
```

保持所有公共公开。私下接触维护人员尽管这很诱人，但不要这样做，除非您需要共享敏感信息(比如安全问题或严重的行为违规)。当你公开谈话时，更多的人可以从你的交流中学习和受益。讨论本身就是贡献。

```
  (as a comment) “@-maintainer Hi there! How should we proceed on this PR?”

  (as an email) “Hey there, sorry to bother you over email, but I was wondering 
  if you’ve had a chance to review my PR”
```

问问题是可以的(但要有耐心!)每个人在某个时候对这个项目都很陌生，即使是经验丰富的贡献者在他们看到一个新项目时也需要加快速度。出于同样的原因，即使是长期的维护人员也不总是熟悉项目的每个部分。向他们展示你希望他们展示给你的耐心。

```
  “Thanks for looking into this error. I followed your suggestions. Here’s the output.”

  “Why can’t you fix my problem? Isn’t this your project?”
```

尊重社区的决定。您的想法可能与社区的优先级或远景不同。他们可能会提供反馈，或者决定不遵从你的想法。您应该讨论并寻找妥协，维护人员认同你的决策所用的时间比你自己所用时间要长。如果你不同意他们的观点，你就可以自己动手fork，开始自己的项目。

```
  “I’m disappointed you can’t support my use case, but as you’ve explained it
   only affects a minor portion of users, I understand why. Thanks for listening.”


  “Why won’t you support my use case? This is unacceptable!”
```

最重要的是，保持优雅。开源是由来自世界各地的合作者组成的。上下文在跨越语言、文化、地理和时区时丢失。此外，书面交流也使得表达语气或情绪变得更加困难。在这些对话中预设良好的意图。你可以礼貌地拒绝一个想法，询问更多的背景信息，或者进一步阐明你的立场。努力让互联网变成一个更好的地方。

##### 收集场景上下文

在做任何事情之前，先快速检查一下，确保你的想法没有在其他地方讨论过。略去项目的自述、问题(打开和关闭)、邮件列表和堆栈溢出。你不需要花几个小时浏览每一件事，但是快速搜索几个关键的词汇会大有帮助。

如果你在别的地方找不到你的想法，你就准备好采取行动了。如果项目在GitHub上，您可能会通过打开一个问题或拉出pull request来进行沟通:

- issues就像开始谈话或讨论一样

- pullrequest是用来启动解决方案的。

- 对于轻量级的通信，比如澄清或操作的问题，试着询问Stack Overflow、IRC、Slack或其他聊天频道, 如果项目有的话。

在打开问题或pull request之前，检查项目的贡献文档(通常是一个名为贡献的文件，或者在自述文件中)，看看是否需要包含任何特定的内容。例如，他们可能会要求您遵循一个模板，或者要求您使用测试。

如果你想做出实质性的贡献，在着手解决之前，先提出一个issue。在GitHub上看一段时间的项目是很有帮助的(在GitHub上，你可以点击“watch”来获知所有的对话)，在工作之前了解社区成员， 不然很可能不会被接受。

> You’ll learn a lot from taking a single project you actively use, “watching” it 
on GitHub and reading every issue and PR. — @gaearon on joining projects

### open一个问题

你通常应该在以下情况下提出一个问题:


- 报告一个你自己无法解决的错误

- 讨论一个高级主题或想法(例如，社区、远景或策略)

- 提出一个新特性或其他项目想法

沟通问题的技巧:


- 如果你看到一个你想要解决的公开问题，就评论这个问题，让人们知道你正在处理它。这样，人们就不太可能重复你的工作。

- 如果一个问题是在一段时间之前打开的，那么它可能正在其他地方被处理，或者已经被解决，所以请在开始工作之前请求确认。

- 如果你打开了一个问题，但后来自己找到了答案，那么就对这个问题发表评论，让人们知道，然后结束这个问题。甚至记录这个结果也是对项目的贡献。

##### 打开一个pull request

在下列情况下，你通常应该打开一个pull请求:


- 提交琐碎的修复(例如，一个错误、一个坏链接或一个明显的错误)

- 开始做一个已经被要求的贡献，或者你已经讨论过的问题

pull request并不意味着已经完成的工作。通常情况下，最好是尽早打开一个请求，这样其他人就可以观察或反馈你的进展情况。在subject line上把它标记为“WIP”(正在进行中的工作)即可。以后可以添加更多的提交。


如果项目在GitHub上，下面是提交pull request的方式:


- Fork存储库并在本地克隆它。通过将本地存储库添加为远程存储库，将其连接到原始的“上游”存储库。经常从“上游”中pull更改，以便您保持最新，提交拉请求时，合并冲突的可能性更小。[(请参阅这里的详细说明。)](https://help.github.com/articles/syncing-a-fork/)

- 为变动创建一个[分支](https://guides.github.com/introduction/flow/)。

- 在您的PR中引用任何相关的问题或支持文档(例如，“关闭#37”)。

- 如果您的更改包含HTML/CSS的差异，请包含前后的屏幕截图。将图像拖放到您的拉请求的主体中。

- 测试您的更改!如果存在任何现有的测试，运行您的更改，并在需要时创建新的测试。无论测试是否存在，请确保您的更改不会破坏现有的项目。

- 在项目的风格上尽你最大的努力。这可能意味着使用缩进、半冒号或注释与您在自己的存储库中使用的不同，但是使维护人员更容易合并，其他人更容易在将来理解和维护。

如果这是您的第一个pull request，请查看[案例](http://makeapullrequest.com/)，这是@kentcdodds作为一个演练视频教程创建的。您还可以在@Roshanjossey创建的第一个贡献存储库中练习发出pull request。