---
title: 将Linux作为第二主力系统（一）
date: 2021-12-05 22:40:49
cover: https://images.unsplash.com/photo-1549605659-32d82da3a059
categories:
  - 解决方案
tags:
  - Linux
  - 瞎折腾
---

这段时间刚好搬家，于是获得了一个额外可以放置第二台主力机和一个额外显示器的机会。趁着这个机会，再加上喜欢折腾，于是我决定为这第二台机器装上Linux。在本篇中，我将会讲到为什么要选择Linux、谁更适合Linux以及我会选择的Linux发行。

<!-- more -->

## 为什么选择 Liunx？

其实选择 Linux 的理由很简单。Linux 是一个开源、开放、可定制性强的操作系统。而且相对偏向开发者群体。所以这对我一个喜欢折腾的业余开发来说，在合适不过了。当然 Linux 相对于 Windows还有两个优点，就是系统占用的资源小，而且不强制使用某些硬件（例如 TPM 2.0）。对我来说，这两个优点是个非常重要的，具体的我会在以后安装系统时再提。

## 谁会适合使用 Linux？

Linux 并非适合所有人，其实大部分人都不太适合。先不说部分 Linux 的配置繁琐，大部分的 Linux 桌面环境（Desktop Environment）的体验都不如 Winodws 和 macOS。而且部分，甚至是大部分常用软件都与 Linux（至少是一部分发行版）有兼容问题。所以，到底谁不适合使用 Linux 呢？如果你希望所有的都交给操作系统，基本上不需要考虑驱动的问题，设置全靠自动，安装软件只想下一步，换句话说只想开箱即用完全不折腾的话，Linux 并不适合你。如果你一看需要命令行就头疼，Linux 不适合你。如果你遇到问题完全不想查资料，Linux 还是不适合你。如果你经常使用的一些软件完全不支持 Linux 并且没有很好的解决/替代方案时，Linux 也不适合你。那到底谁适合使用 Linux？如果你喜欢定制你的系统，愿意折腾的话，Linux 是个不错的选择。如果你喜欢折腾，在遇到问题时有时间**而且愿意**查询各种解决方案和各种文档，Linux 也适合你。同时，鉴于 Linux 在开发环境中的优势，使用 Linux 写代码总体来说会是个挺不错的选择。

## 我会考虑使用的 Linux 发行

{% note color:red 本列表中列出的是我在确定要更换系统是立即想到的几个我可能会经常使用的操作系统，并非操作系统排名，也并不会列出所有操作系统，仅为根据个人习惯进行的选择。 %}

### CentOS/Rocky Linux/其他RHEL下游
由于都是RHEL的下游，所以我把它们放在了一起。RHEL以及下游是个非常优秀的操作系统。稳定而且安全。但是由于是服务器操作系统，并不谁非常适合日常使用，故暂不考虑。（如果仅做开发的话，其实这几个系统也非常优秀。）我基本上所有的服务器都在使用这些操作系统。

提醒：CentOS Stream并不包含在其中，而CentOS也将只会继续更新维护Stream。

### Ubuntu
Ubuntu 可能是新手们认识到的第一个 Linux 了，开箱即用且易于上手，但是由于长期使用RHEL操作系统，我早已习惯RHEL系列的包管理器等工具，因此暂不考虑。

### Fedora
RHEL上游操作系统。与RHEL以及下游操作系统本质上并无太多差别。包管理器等工具也都是相同的。最大的不同是，Fedora的操作系统是滚动更新的，这意味着Fedora会比其他RHEL体系中的系统更早收到新功能，但这也意味着安全性和稳定性相对的降低。不过对于日常使用来说，这些缺失带来的问题并不会像在服务器环境下那么严重。因此，Fedora 还是目前最常用的 Linux 工作站操作系统之一。而且 Fedora 也有一个第三方组织 [Fedora Spins](https://spins.fedoraproject.org) 提供着预装着个大桌面环境的 Fedora ISO。同时，由于我对RHEL系列较为熟悉，所以Fedora将会是我优先选择的操作系统之一。

{% note color:yellow 在此提一句，RHEL体系的更新顺序（从上游排名到下游）为： Fedora -> CentOS Stream -> RHEL -> CentOS、Rocky等下游 %}

### Arch Linux

Arch Linux 一直以极高的定制度闻名。但是，我目前更偏向适用一个相对可以开箱即用的操作系统，所以暂不考虑。

### Artix Liunx

Artix Linux 是个基于 Arch Linux 的操作系统，相对原本的 Arch，Artix 已经为用户进行了一些配置，但是仍然保留着很大的定制度。而且不使用 systemd。但是由于并不算很火，网络上缺乏各种教程等材料，所以暂时也不考虑。

### Manjaro

基于 Arch 的 Linux 中最新手友好的操作系统。Manjaro 官方为其提供了不少的软件，而且官方也提供了大部分常用桌面环境的ISO。在对新手如此友好的同时，Arch Linux 高定制度等原本的优势也被 Manjaro 保留了。同时，由于 Manjraro 在社区的知名度，网络上也存在不少 Manjaro 相关的教程等内容。所以 Manjaro 也会是我备选系统之一。


## 下一步

在真正的向实体机安装操作系统之前，我将会在虚拟机内先安装我目前唯二真正的备选操作系统：Fedora 和 Manjaro。我将会使用我最常用的 KDE Plasma 桌面，虚拟机统一分配2核心CPU，4GB内存。我会在接下来一段时间内定期更新这两个操作系统的使用体验，并最终决定使用哪个系统。

## 对了

我也准备将 Arch 安装在虚拟机中，这样想折腾系统的时候可以玩玩。相对于实体机，虚拟机对完炸了的情况下的备份和回滚更加方便。所以，喜欢折腾的各位不妨试试。

## 结语

对于喜欢折腾的人来说，在一个相对性能已经不够 Windows 使用的电脑上安装 Linux 并偶尔使用不失为一个好方法。当然，鉴于目前的情况，Linux 仍然不适合普通用户 100% 日常使用。但是，如果你想找点事做，折腾一把，不妨试试 Linux，GL&HF!