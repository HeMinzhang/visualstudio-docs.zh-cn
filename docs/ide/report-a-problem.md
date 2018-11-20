---
title: "综述：在Visual Studio中报告问题"
description: "Provides an overview of the Report a Problem tool, and includes problem states and definitions"
ms.date: 11/15/2018
ms.prod: visual-studio-dev15
ms.technology: vs-acquisition
ms.topic: conceptual
author: seaniyer
ms.author: seiyer
manager: douge
ms.workload:
  - "multiple"
---
# 综述：报告问题

报告问题工具使Visual Studio开发者社区可以提交问题。你报告的每个问题都变成我们工程师团队的核心工作项，使你能参与帮助我们产品团队识别和解决有影响力的问题。提交丰富诊断信息的反馈对改善Visual Studio产品系列至关重要。我们感谢您花时间报告问题。

另外，您可以对其他社区成员的反馈进行投票，以便更多地关注问题并帮助您更快地解决问题。

## 问题状态

在你报告问题之后，报告问题的生命周期通过状态表明。当微软团队检查你的反馈时，他们将会设置一个适当的状态。通过参考下面列出的状态来跟踪问题报告的进度，以及它们的含义和颜色标志。

![在开发者社区中新问题状态](../ide/media/ProblemStates/New.jpg)

**新** 表示bug或者问题是最新报告的，并没有采取任何行动。

- - -

![Triaged state for problem reporting on Developer Community](../ide/media/ProblemStates/Triaged.jpg)

**Triaged** indicates that preliminary steps such as moderation, translation, and  initial check for duplicates are  complete. Your ticket has been routed to the appropriate engineering team for consideration.

- - -

![Under Consideration state for problem reporting on Developer Community](../ide/media/ProblemStates/UnderConsideration.jpg)

**Under Consideration** indicates that Microsoft is reviewing your problem for community impact and will prioritize it accordingly. If the community impact isn't clear or significant yet, we'll continue to monitor the problem in this state.

- - -

![Under Investigation state for problem reporting on Developer Community](../ide/media/ProblemStates/UnderInvestigation.jpg)

**Under Investigation** indicates that engineers are actively investigating your problem to find a resolution.

- - -

![Need More Info state for problem reporting on Developer Community](../ide/media/ProblemStates/NeedMoreInfo.jpg)

**Need More Info** indicates that we need more diagnostic information from you so that we can go forward with the investigation.  [Learn how to respond to Need More Info requests.](./how-to-report-a-problem-with-visual-studio-2017.md#when-further-information-is-needed-need-more-info)

- - -

![Fixed - Pending Release state for problem reporting on Developer Community](../ide/media/ProblemStates/FixedPendingRelease.jpg)

**Fixed - Pending Release** indicates that we have a fix for the problem and it will be available in an upcoming preview or release.  When the fix becomes available in a preview, the problem is tagged with a 'fixed in' tag specifying the preview version.

- - -

![Closed - Fixed state for problem reporting on Developer Community](../ide/media/ProblemStates/ClosedFixed.jpg) 

**Closed - Fixed** indicates that we've released a fix for the problem. The problem is also now tagged with a "fixed in:" tag specifying the release version.

- - -

![Closed - Duplicate state for problem reporting on Developer Community](../ide/media/ProblemStates/ClosedDuplicate.jpg)

**Closed - Duplicate** indicates that your issue has already been reported via another feedback. We'll provide you with the link where you can track the original problem report.

- - -

![Closed - Lower Priority state for problem reporting on Developer Community](../ide/media/ProblemStates/ClosedLowerPriority.jpg)

**Closed - Lower Priority** To focus on bringing each of you in our developer community the best value, we prioritize issues with the highest customer impact. Although we're unable to address this particular issue at this time, be assured that all your feedback is valuable and helps improve Visual Studio.

- - -

![Closed - Not a Bug state for problem reporting on Developer Community](../ide/media/ProblemStates/ClosedNotaBug.jpg)

**Closed - Not a Bug**  indicates that we've determined that the reported functionality is by current design.

- - -

![Closed - Not Enough Info state for problem reporting on Developer Community](../ide/media/ProblemStates/ClosedNotEnoughInfo.jpg)

**Closed - Not Enough Info** indicates that we don't have enough information to investigate this for you. We'll be happy to reconsider the feedback after the necessary information is available.

- - -

![Closed - Other Product state for problem reporting on Developer Community](../ide/media/ProblemStates/ClosedOtherProduct.jpg)

**Closed - Other Product** indicates we've determined that your issue applies to another product. See the comment from Microsoft for which external product and any related links.

- - -

![Closed - Won't Fix state for problem reporting on Developer Community](../ide/media/ProblemStates/ClosedWontFix.jpg)

**Closed - Won't Fix** indicates that we aren't pursuing this issue due to factors such as lack of product direction alignment or community impact. See the comment from Microsoft for any additional clarity.  Although we're unable to address this particular issue, be assured that all your feedback is valuable and helps improve Visual Studio.

- - -

## FAQ

### How can I increase the chance of my problem getting resolved quickly?

We recommend using search to ensure that the problem you're about to report hasn't already been reported. If you find an existing item matching your problem, follow and vote on that problem ticket.

 Provide all the information you can to help our teams reproduce what you're experiencing.  This information includes  necessary repro steps, code fragments, screenshots, repro recordings, log files, and other artifacts.  Here is [how to report a problem in Visual Studio](./how-to-report-a-problem-with-visual-studio-2017.md).

### How is my feedback prioritized?

We receive a large number of valuable problems from our customers. To ensure that we're bringing the best value to each of you in our developer community, we prioritize action on feedback that has the highest community impact.

If we aren't able to respond personally to your feedback, know that we fully appreciate your input. Be assured that all your feedback gets to the right team.

We truly value the time you invest in making Visual Studio better.

### What actions can I take if I'm not satisfied with the resolution?

Our teams do their best to diagnose and fix any issues you experience, however there may be times when you're not fully satisfied with our recommendation. Comment back on the feedback and let us know exactly what you're not satisfied with, and we'll try our best to ensure that we meet your needs.

### How will I get notified of progress on my feedback?

Microsoft engineering teams will communicate with you by commenting on the feedback ticket and changing the state of your ticket as they make progress. Watch for e-mail notifications that are sent when  ticket state changes or a comment is posted.  You can manage frequency of notifications in Profile and Preferences settings on Developer Community site.

### Why can't I add a problem for Visual Studio IDE on the Developer Community website?

Reporting a problem through Visual Studio allows for diagnostic information to automatically be included in the report. It's essential information that gives our engineers the context they need to fully understand your issue and work to resolve it.

When you report through Visual Studio, you can easily share rich diagnostic information with us, such as large log files, crash information, screenshots, repro recording, and other artifacts that help us deliver higher-quality resolutions faster to you.