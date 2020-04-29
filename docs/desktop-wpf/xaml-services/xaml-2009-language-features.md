---
title: XAML 2009 语言功能
ms.date: 03/30/2017
helpviewer_keywords:
- XAML 2009 [XAML Services]
- XAML [XAML Services], XAML 2009
ms.assetid: f6bb18d8-c86a-4549-8862-323e6b32a8dd
ms.openlocfilehash: e58e6757b88958bf8a3547c8a272c2e6298dcecb
ms.sourcegitcommit: c2d9718996402993cf31541f11e95531bc68bad0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/27/2020
ms.locfileid: "81432838"
---
# <a name="xaml-2009-language-features"></a><span data-ttu-id="610a3-102">XAML 2009 语言功能</span><span class="sxs-lookup"><span data-stu-id="610a3-102">XAML 2009 Language Features</span></span>
<span data-ttu-id="610a3-103">XAML 2009 是新 XAML 语言功能的简写术语，其扩展现有的 XAML 语言规范。</span><span class="sxs-lookup"><span data-stu-id="610a3-103">XAML 2009 is the shorthand term for new XAML language features that extend the existing XAML language specification.</span></span> <span data-ttu-id="610a3-104">XAML 2009 引入了几个新指令和结构。</span><span class="sxs-lookup"><span data-stu-id="610a3-104">XAML 2009 introduces several new directives and constructs.</span></span> <span data-ttu-id="610a3-105">其中包括[x：参数指令](xarguments-directive.md);[x：工厂方法指令](xfactorymethod-directive.md);[x：参考标记扩展](xreference-markup-extension.md);[x：类型参数指令](xtypearguments-directive.md);和通用语言基元（例如`x:Char`）的内置类型。</span><span class="sxs-lookup"><span data-stu-id="610a3-105">These include the [x:Arguments Directive](xarguments-directive.md); the [x:FactoryMethod Directive](xfactorymethod-directive.md); the [x:Reference Markup Extension](xreference-markup-extension.md); the [x:TypeArguments Directive](xtypearguments-directive.md); and built-in types for common language primitives (for example `x:Char`).</span></span>

## <a name="xaml-2009-support-in-wpf-and-visual-studio"></a><span data-ttu-id="610a3-106">在 WPF 和 Visual Studio 中支持 XAML 2009</span><span class="sxs-lookup"><span data-stu-id="610a3-106">XAML 2009 Support in WPF and Visual Studio</span></span>

<span data-ttu-id="610a3-107">在 WPF 中，可以使用 XAML 2009 功能，但仅针对未进行 WPF 标记编译的 XAML。</span><span class="sxs-lookup"><span data-stu-id="610a3-107">In WPF, you can use XAML 2009 features, but only for XAML that is not WPF markup-compiled.</span></span> <span data-ttu-id="610a3-108">标记编译的 XAML 以及 BAML 形式的 XAML 当前不支持 XAML 2009 语言关键字和功能。</span><span class="sxs-lookup"><span data-stu-id="610a3-108">Markup-compiled XAML and the BAML form of XAML do not currently support the XAML 2009 language keywords and features.</span></span>

<span data-ttu-id="610a3-109">请注意，在 WPF 中加载松散的 XAML 的现有技术也有可能受到 CLR 类型的安全和访问限制，该类型系统比标记编译的 XAML 更加严格。</span><span class="sxs-lookup"><span data-stu-id="610a3-109">Note that existing techniques for loading loose XAML in WPF also have possible security and access restrictions to CLR types and the type system that are more restrictive than for markup-compiled XAML.</span></span> <span data-ttu-id="610a3-110">有关更多信息，请参见 [安全性 (WPF)](../../framework/wpf/security-wpf.md) 或 [WPF 安全策略 — 平台安全性](../../framework/wpf/wpf-security-strategy-platform-security.md)。</span><span class="sxs-lookup"><span data-stu-id="610a3-110">For more information, see [Security (WPF)](../../framework/wpf/security-wpf.md) or [WPF Security Strategy - Platform Security](../../framework/wpf/wpf-security-strategy-platform-security.md).</span></span>

<span data-ttu-id="610a3-111">XAML 2009 还引入了一些附加功能，可修改曾经的 XAML 2006 构造或修改基本标记窗体。</span><span class="sxs-lookup"><span data-stu-id="610a3-111">XAML 2009 also introduces additional features that either modify the previous XAML 2006 constructs or that modify the basic markup forms.</span></span>

### <a name="xkey-as-an-object-element"></a><span data-ttu-id="610a3-112">X:key 作为对象元素</span><span class="sxs-lookup"><span data-stu-id="610a3-112">x:Key as an Object Element</span></span>

<span data-ttu-id="610a3-113">XAML 2009 可支持 `x:Key` 作为对象（具有对象元素值的属性元素）；但是 XAML 2006 仅支持 `x:Key` 作为属性。</span><span class="sxs-lookup"><span data-stu-id="610a3-113">XAML 2009 can support `x:Key` as an object (a property element that has object element value); however, XAML 2006 only supported `x:Key` as an attribute.</span></span> <span data-ttu-id="610a3-114">请参阅 [x:Key Directive](xkey-directive.md)的“XAML 2009”一节。</span><span class="sxs-lookup"><span data-stu-id="610a3-114">See the "XAML 2009" section of [x:Key Directive](xkey-directive.md).</span></span>

### <a name="xmlns-on-property-elements"></a><span data-ttu-id="610a3-115">属性元素上的 xmlns</span><span class="sxs-lookup"><span data-stu-id="610a3-115">xmlns on Property Elements</span></span>

<span data-ttu-id="610a3-116">XAML 2009 可以支持属性元素上的 XAML 命名空间 (xmlns) 定义，而 XAML 2006 只支持对象元素上的 xmlns 定义。</span><span class="sxs-lookup"><span data-stu-id="610a3-116">XAML 2009 can support XAML namespace (xmlns) definitions on property elements; however, XAML 2006 only supports xmlns definitions on object elements.</span></span>

### <a name="event-attributes"></a><span data-ttu-id="610a3-117">事件特性</span><span class="sxs-lookup"><span data-stu-id="610a3-117">Event Attributes</span></span>

<span data-ttu-id="610a3-118">对于由事件支持的特性，XAML 2006 会假定涉及到了标记编译并将事件提交给标记编译。</span><span class="sxs-lookup"><span data-stu-id="610a3-118">For attributes that are backed by events, XAML 2006 presumes that markup compilation is involved and submits the events to markup compilation.</span></span> <span data-ttu-id="610a3-119">XAML 2009 支持类似标记扩展的标记窗体，其不同于事件布线，直至运行时解析/加载 XAML。</span><span class="sxs-lookup"><span data-stu-id="610a3-119">XAML 2009 supports a markup form that resembles a markup extension, which defers the event wiring until run-time parsing and loading of the XAML.</span></span> <span data-ttu-id="610a3-120">但是，WPF 应用程序和 WPF UI 的 XAML 方案通常不使用此功能。</span><span class="sxs-lookup"><span data-stu-id="610a3-120">However, WPF applications and XAML scenarios for WPF UI generally do not use this capability.</span></span> <span data-ttu-id="610a3-121">WPF 和其 XAML 2006 实现使用在 <xref:System.Windows.UIElement> 级别定义的路由事件的事件处理程序布线组合及其标记编译器步骤，用于其众多事件特性处理。</span><span class="sxs-lookup"><span data-stu-id="610a3-121">WPF and its XAML 2006 implementation uses the combination of event handler wiring for routed events defined at the <xref:System.Windows.UIElement> level and its markup compiler step for much of its event attribute processing.</span></span> <span data-ttu-id="610a3-122">标记编译器还预处理生成操作声明用于标记编译器的 XAML 中找到任何事件属性。</span><span class="sxs-lookup"><span data-stu-id="610a3-122">The markup compiler also preprocesses any event attributes found in XAML where the build actions declare that the markup compiler is used.</span></span>

## <a name="see-also"></a><span data-ttu-id="610a3-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="610a3-123">See also</span></span>

- [<span data-ttu-id="610a3-124">XAML 概述 (WPF)</span><span class="sxs-lookup"><span data-stu-id="610a3-124">XAML Overview (WPF)</span></span>](../fundamentals/xaml.md)