---
ms.openlocfilehash: 88a0b7e04c7015ca3fa5abd8a6897dafcbe41c49
ms.sourcegitcommit: 8bfeb5930ca48b2ee6053f16082dcaf24d46d221
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/18/2020
ms.locfileid: "88557955"
---
### <a name="multicastoptiongroup-doesnt-accept-a-null-value"></a>MulticastOption.Group 不接受 null 值

<xref:System.Net.Sockets.MulticastOption.Group?displayProperty=nameWithType> 不再接受 `null` 值。 如果将属性设置为 `null`，则会引发 <xref:System.ArgumentNullException>。

#### <a name="version-introduced"></a>引入的版本

5.0

#### <a name="change-description"></a>更改描述

在早期版本的 .NET 中，可以将 <xref:System.Net.Sockets.MulticastOption.Group?displayProperty=nameWithType> 属性设置为 `null`。 如果 <xref:System.Net.Sockets.MulticastOption> 稍后传递给 <xref:System.Net.Sockets.Socket.SetSocketOption%2A?displayProperty=nameWithType>，则运行时将引发 <xref:System.NullReferenceException>。

在 .NET 5.0 和更高版本中，如果将属性设置为 `null`，则会引发 <xref:System.ArgumentNullException>。

#### <a name="reason-for-change"></a>更改原因

为了与框架设计准则保持一致，属性已更新为在值为 `null` 时引发 <xref:System.ArgumentNullException>。

#### <a name="recommended-action"></a>建议操作

请确保未将 <xref:System.Net.Sockets.MulticastOption.Group?displayProperty=nameWithType> 设置为 `null`。

#### <a name="category"></a>类别

网络

#### <a name="affected-apis"></a>受影响的 API

- <xref:System.Net.Sockets.MulticastOption.Group?displayProperty=fullName>

<!--

#### Affected APIs

- `P:System.Net.Sockets.MulticastOption.Group`

-->
