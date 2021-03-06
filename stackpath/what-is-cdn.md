# ![](/assets/cdn-demo.png)

# 什么是 CDN（Content Delivery Network）

## 概述

Web服务的性能和可靠性是直接影响盈利能力和客户满意度的主要因素。为了改善这些因素，开发人员利用 CDN 来缓存（存储）和传送网页内容。这包括静态资源，如图像，视频，CSS，JavaScript 和文件下载。

通过在 CDN 上缓存资源，资源分布在物理位置上距离用户最近的地方，从而提高了页面的加载速度。除了在 CDN 上缓存静态资源外，Web 开发人员还可以通过 CDN 来移植动态内容，从而绕过互联网服务提供商（[ISP](https://en.wikipedia.org/wiki/Internet_service_provider)）可能存在的网络拥塞。

## CDN 是怎样工作的？

当一个用户访问没有使用 CDN 的一个网站时，他下载的静态资源是在一个单一的源站点。如果这个静态资源服务器的物理位置在纽约而用户在日本，那个他的每个资源下载将会穿越几乎整个地球。在这样的情况下，由于下载的延迟用户加载这个页面需要很长的时间。

CDN 将文件分布在全球的各个服务器上，从而减少了访问文件所需要的时间。举个例子，身在日本的用户可以从在亚洲附近的服务器上下载文件而不是从远在北美的服务器上下载。

下面是一个 CDN 工作流程的例子：

1. 开发者在 CDN 提供商为 example.com 这个源站点注册了服务，CDN 提供商给开发者提供了 CDN 专业的 URL 如 site-alias.stackpathdns.com（CDN 提供商就比如是StackPath）。
2. 开发人员给站点配置 URL 让资源从 CDN 上加载而不是直接从源站。像 WordPress 这种软件可以通过一些插件来实现。
3. 一个用户在浏览器中访问了 example.com。浏览器使用 CDN URL来请求页面中内联的静态资源比如：site-alias.stackpathdns.com/image.png。
4. CDN 自动将请求分发到距离该请求物理位置最近的服务器，其使用像了 DNS 负载平衡和任播路由等技术。之前还么有存储在 CDN 上的资源将会去源站获取，并存储在 CDN 上为之后的请求服务。
5. 浏览器从距离自己较近的地方下载资源，既提升了网页加载的性能，同时也减轻了源站访问的压力。

## CDN 的例子

许多开发者使用了第三方库如 [Twitter Bootstrap](http://getbootstrap.com/) 来改善他们的布局和功能。但是，开发人员可能不希望在源站托管这些库，以节省带宽成本并提高性能。

像 [BootstrapCDN](http://www.bootstrapcdn.com/) 这种开源 CDN 让用户从 CDN 加载 Twitter Bootstrap 的 CSS、JavaScript 文件。这减少了服务器负载并加速了用户的访问。此外，如果用户已经访问了使用 BootstrapCDN 上相同文件的站点，用户可以避免重新下载这些文件。

### 结论

在具有一定规模的 Web 应用程序中，CDN 是一种流行的方式来分配流量为了使得访问更加迅速、可靠。在一个产品中使用 CDN 解决方案时，用户从第三方服务器下载资源而不是从源站。这提高了性能，也减少了公司建立和维护自己的全球网络的需要。当谈到 Web服务和在线体验的实际交付时，开发者可以依靠 CDN 来进行改善。

Translate from

[https://blog.stackpath.com/glossary/cdn/](https://blog.stackpath.com/glossary/cdn/)

