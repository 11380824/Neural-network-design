#Preface

```
前言
```

This book gives an introduction to basic neural network architectures and learning rules. Emphasis is placed on the mathematical analysis of these networks, on methods of training them and on their application to practical engineering problems in such areas as nonlinear regression, pattern recognition, signal processing, data mining and control systems.

```
本书介绍了基础神经网络架构和学习规则。 重点放在神经网络的数学分析，训练方法及其在非线性回归，模式识别，信号处理，数据挖掘和控制系统等方面的实际工程问题上。
```

Every effort has been made to present material in a clear and consistent manner so that it can be read and applied with ease. We have included many solved problems to illustrate each topic of discussion. We have also included a number of case studies in the final chapters to demonstrate practical issues that arise when using neural networks on real world problems.

```
已尽一切努力以清晰和一致的方式呈现材料，使本书可以轻松阅读和应用。 我们已经包含了很多已解决的问题来说明每个讨论的话题。 在最后的章节中，我们还包括了一些案例研究，以展示在现实世界问题中使用神经网络时出现的实际问题。

```
Since this is a book on the design of neural networks, our choice of topics was guided by two principles. First, we wanted to present the most useful and practical neural network architectures, learning rules and training
techniques. Second, we wanted the book to be complete in itself and to flow easily from one chapter to the next. For this reason, various introductory materials and chapters on applied mathematics are included just before
they are needed for a particular subject. In summary, we have chosen some topics because of their practical importance in the application of neural networks, and other topics because of their importance in explaining how neural networks operate.

```
由于这是一本关于神经网络设计的书，所以我们选择的话题是由两个原则指导的。 首先，我们想要展示最有用和最实用的神经网络架构，学习规则和训练技术。 其次，我们希望本书能够完整和流畅地从一章到下一章进行介绍。 出于这个原因，前面已经包括了应用数学的各种介绍性材料和章节他们是一个特定的主题需要。 总之，我们选择了一些主题，因为它们在神经网络应用中的实际重要性以及其他主题，因为它们在解释神经网络如何操作方面的重要性。
```

We have omitted many topics that might have been included. We have not, for instance, made this book a catalog or compendium of all known neural network architectures and learning rules, but have instead concentrated on the fundamental concepts. Second, we have not discussed neural network implementation technologies, such as VLSI, optical devices and parallel computers. Finally, we do not present the biological and psychological foundations of neural networks in any depth. These are all important top- ics, but we hope that we have done the reader a service by focusing on those topics that we consider to be most useful in the design of neural networks and by treating those topics in some depth.

```
我们省略了许多可能包含的主题。 例如，我们没有把这本书作为所有已知的神经网络结构和学习规则的目录或概要，而是集中在基本概念上。 其次，我们还没有讨论VLSI(超大规模集成电路)，光学器件和并行计算机等神经网络实现技术。 最后，我们没有深入介绍神经网络的生物学和心理学基础。 这些都是重要的热门话题，但是我们希望通过把重点放在那些我们认为在神经网络设计中最有用的主题，并通过深入处理这些主题，来为读者提供服务。
```

This book has been organized for a one semester introductory course in neural networks at the senior or first year graduate level. (It is also suitable for short courses, self-study and reference.) The reader is expected to have some background in linear algebra, probability and differential equations.

```
本书在高年级或者一年级的研究生阶段就已经组织完成了一个学期的神经网络入门课程。 （也适用于短期课程，自学和参考）。读者期待读者在线性代数，概率和微分方程方面有一定的背景。
```

Each chapter of the book is divided into the following sections: Objectives, Theory and Examples, Summary of Results, Solved Problems, Epilogue, Further Reading and Exercises. The Theory and Examples section comprises the main body of each chapter. It includes the development of fundamental ideas as well as worked examples (indicated by the icon shown here in the left margin). The Summary of Results section provides a convenient listing of important equations and concepts and facilitates the use of the book as an industrial reference. About a third of each chapter is devoted to the Solved Problems section, which provides detailed examples for all key concepts.

```
本书的每一章分为以下几部分：目标，理论与实例，结果总结，解决问题，结语，深入阅读与练习。 理论和实例部分包括每章的主体。 它包括基本思想的发展以及工作实例（在左边显示的图标）。 “结果摘要”部分提供了重要方程式和概念的便利列表，并有助于将本书作为工业参考。 每章大约三分之一专门用于解决问题部分，其中提供了所有关键概念的详细示例。
```

The following figure illustrates the dependencies among the chapters.

```
下图说明了各章之间的依赖关系。
```

![dependencies.jpg](https://github.com/11380824/Neural-network-design/blob/master/Screenshots/dependencies.jpg)

Chapters 1 through 6 cover basic concepts that are required for all of the remaining chapters. Chapter 1 is an introduction to the text, with a brief historical background and some basic biology. Chapter 2 describes the basic neural network architectures. The notation that is introduced in this chapter is used throughout the book. In Chapter 3 we present a simple pat- tern recognition problem and show how it can be solved using three differ- ent types of neural networks. These three networks are representative of the types of networks that are presented in the remainder of the text. In addition, the pattern recognition problem presented here provides a common thread of experience throughout the book.

```
第1章到第6章涵盖了剩余章节所需的基本概念。 第一章是对文本的介绍，简要的历史背景和一些基本的生物学。 第2章介绍了基本的神经网络架构。 本章介绍的符号在本书中使用。 在第3章中，我们提出一个简单的模式识别问题，并说明如何使用三种不同类型的神经网络来解决这个问题。 这三个网络是本文其余部分介绍的网络类型的代表。 另外，这里给出的模式识别问题在本书中提供了一个共同的经验。
```

Much of the focus of this book will be on methods for training neural networks to perform various tasks. In Chapter 4 we introduce learning algorithms and present the first practical algorithm: the perceptron learning rule. The perceptron network has fundamental limitations, but it is important for historical reasons and is also a useful tool for introducing key concepts that will be applied to more powerful networks in later chapters.

```
本书的大部分重点将放在训练神经网络执行各种任务的方法上。 第四章介绍学习算法，介绍第一种实用算法：感知器学习规则。 感知器网络具有根本性的局限性，但是由于历史的原因，这也是一个很有用的工具，可以在后面的章节中介绍应用于更强大网络的关键概念。
```

One of the main objectives of this book is to explain how neural networks operate. For this reason we will weave together neural network topics with important introductory material. For example, linear algebra, which is the core of the mathematics required for understanding neural networks, is reviewed in Chapters 5 and 6. The concepts discussed in these chapters will be used extensively throughout the remainder of the book.

```
本书的主要目标之一是解释神经网络如何运作。 出于这个原因，我们将把神经网络主题与重要的介绍材料结合在一起。 例如，线性代数（这是理解神经网络所需的数学的核心）在第五章和第六章中进行了介绍。这些章节中讨论的概念将在本书的其余部分被广泛使用。
```

Chapters 7, and 15–19 describe networks and learning rules that are heavily inspired by biology and psychology. They fall into two categories: associative networks and competitive networks. Chapters 7 and 15 introduce basic concepts, while Chapters 16–19 describe more advanced networks.

```
第7章和第15-19章描述了深受生物学和心理学启发的网络和学习规则。 它们分为两类：联想网络和竞争网络。 第7章和第15章介绍基本概念，第16-19章介绍更高级的网络。
```

Chapters 8–14 and 17 develop a class of learning called performance learn- ing, in which a network is trained to optimize its performance. Chapters 8 and 9 introduce the basic concepts of performance learning. Chapters 10– 13 apply these concepts to feedforward neural networks of increasing pow- er and complexity, Chapter 14 applies them to dynamic networks and Chapter 17 applies them to radial basis networks, which also use concepts from competitive learning.

```
第8-14章和第17章提出了一种称为性能学习的学习方式，在这种学习中，网络被训练以优化其性能。 第8章和第9章介绍了性能学习的基本概念。 第10-13章将这些概念应用于增加功率和复杂度的前向神经网络，第14章将它们应用于动态网络，第17章将它们应用于径向基础网络，也使用竞争学习的概念。
```

Chapters 22–27 are different than the preceding chapters. Previous chapters focus on the fundamentals of each type of network and their learning rules. The focus is on understanding the key concepts. In Chapters 22–27, we discuss some practical issues in applying neural networks to real world problems. Chapter 22 describes many practical training tips, and Chapters 23–27 present a series of case studies, in which neural networks are applied to practical problems in function approximation, probability estimation, pattern recognition, clustering and prediction.

```
第22-27章与前面的章节不同。 以前的章节着重于每种网络的基本原理和学习规则。 重点是理解关键概念。 在第22-27章中，我们讨论将神经网络应用于现实世界问题的一些实际问题。 第22章介绍了许多实用的训练技巧，第23-27章介绍了一系列案例研究，其中神经网络应用于函数逼近，概率估计，模式识别，聚类和预测等实际问题。
```

MATLAB is not essential for using this book. The computer exercises can be performed with any available programming language, and the Neural Network Design Demonstrations, while helpful, are not critical to under- standing the material covered in this book.

```
MATLAB对使用本书不是必不可少的。 计算机练习可以用任何可用的编程语言来执行，而神经网络设计演示虽然有帮助，但对于理解本书所涵盖的内容并不重要。
```

However, we have made use of the MATLAB software package to supplement the textbook. This software is widely available and, because of its matrix/vector notation and graphics, is a convenient environment in which to experiment with neural networks. We use MATLAB in two different ways. First, we have included a number of exercises for the reader to perform in MATLAB. Many of the important features of neural networks become apparent only for large-scale problems, which are computationally intensive and not feasible for hand calculations. With MATLAB, neural network algorithms can be quickly implemented, and large-scale problems can be tested conveniently. These MATLAB exercises are identified by the icon shown here to the left. (If MATLAB is not available, any other programming language can be used to perform the exercises.)

```
但是，我们已经使用MATLAB软件包来补充教科书。 这个软件是广泛使用的，因为它的矩阵/向量记号和图形，是一个方便的环境中，试验神经网络。 我们以两种不同的方式使用MATLAB。 首先，我们已经包含了一些读者在MATLAB中执行的练习。 神经网络的许多重要特征仅适用于大规模问题，计算量大，不适合手工计算。 使用MATLAB，可以快速实现神经网络算法，并且可以方便地测试大规模问题。 这些MATLAB练习由左侧显示的图标标识。 （如果MATLAB不可用，则可以使用任何其他编程语言来执行练习。）
```

The second way in which we use MATLAB is through the Neural Network Design Demonstrations, which can be downloaded from the website hagan.okstate.edu/nnd.html. These interactive demonstrations illustrate important concepts in each chapter. After the software has been loaded into the MATLAB directory on your computer (or placed on the MATLAB path), it can be invoked by typing nnd at the MATLAB prompt. All demonstrations are easily accessible from a master menu. The icon shown here to the left identifies references to these demonstrations in the text.

```
我们使用MATLAB的第二种方式是通过神经网络设计演示，可以从网站hagan.okstate.edu/nnd.html下载。 这些互动演示说明了每章中的重要概念。 在软件加载到您的计算机上的MATLAB目录（或放在MATLAB路径中）后，可以通过在MATLAB提示符处输入nnd来调用该软件。 所有演示都可以从主菜单轻松访问。 这里显示的图标在文本中标识了对这些演示的引用。
```

The demonstrations require MATLAB or the student edition of MATLAB, version 2010a or later. See Appendix C for specific information on using the demonstration software.

```
演示需要MATLAB或MATLAB版本2010a或更高版本的学生版本。 有关使用演示软件的具体信息，请参阅附录C.
```

##Overheads

As an aid to instructors who are using this text, we have prepared a companion set of overheads.Transparency masters (in Microsoft Powerpoint format or PDF) for each chapter are available on the web at hagan.okstate.edu/nnd.html.

```
为了帮助正在使用本书的教师，我们准备了一套相关的资料。 网址 hagan.okstate.edu/nnd.html 提供了每章的幻灯片文件（以Microsoft Powerpoint格式或PDF格式）。
```

We are deeply indebted to the reviewers who have given freely of their time to read all or parts of the drafts of this book and to test various versions of the software. In particular we are most grateful to Professor John Andreae, University of Canterbury; Dan Foresee, AT&T; Dr. Carl Latino, Oklahoma State University; Jack Hagan, MCI; Dr. Gerry Andeen, SRI; and Joan Mill- er and Margie Jenks, University of Idaho. We also had constructive inputs from our graduate students in ECEN 5733 at Oklahoma State University, ENEL 621 at the University of Canterbury, INSA 0506 at the Institut National des Sciences Appliquées and ECE 5120 at the University of Colorado, who read many drafts, tested the software and provided helpful suggestions for improving the book over the years. We are also grateful to the anonymous reviewers who provided several useful recommendations.

```
我们非常感谢广大读者付出时间阅读本书全文或部分内容并测试各个版本的软件。特别感谢坎特伯雷大学的安德里亚教授， AT＆T公司的Dan Foresee; 俄克拉何马州立大学卡尔·拉丁诺博士; MCI的Jack Hagan; SRI的Gerry Andeen博士; 和爱达荷大学的Joan Milller和Margie Jenks。 我们还从俄克拉荷马州立大学的EC33733，坎特伯雷大学的ENEL621，国家科学研究院的INSA0506和科罗拉多大学的ECE5120的研究生那里获得了建设性的意见，他们大量阅读了本书的草稿， 对这些软件进行了测试，并持续多年提供有益的改进建议。 我们同时感谢那些匿名读者提供有用建议。
```

We wish to thank Dr. Peter Gough for inviting us to join the staff in the Electrical and Electronic Engineering Department at the University of Canterbury, Christchurch, New Zealand, and Dr. Andre Titli for inviting us to join the staff at the Laboratoire d'Analyse et d'Architecture des Systèms, Centre National de la Recherche Scientifique, Toulouse, France. Sabbaticals from Oklahoma State University and a year’s leave from the University of Idaho gave us the time to write this book. Thanks to Texas Instruments, Halliburton, Cummins, Amgen and NSF, for their support of our neural network research. Thanks to The Mathworks for permission to use material from the Neural Network Toolbox.

```
我们忠心感谢Peter Gough博士邀请我们加入新西兰基督城坎特伯雷大学电气，电子工程系的工作人员和Andre Titli博士邀请我们加入实验室工作人员，法国图卢兹国家科学研究中心和体系结构分析。俄克拉何马州立大学给予的学术假期，爱达荷大学给予一年的时间让我们有时间写这本书。 感谢德州仪器，哈里伯顿公司，康明斯，安进公司和NSF，为我们的神经网络研究提供支持。 感谢Mathworks获得授权使用Neural Network Toolbox的材料。
```
