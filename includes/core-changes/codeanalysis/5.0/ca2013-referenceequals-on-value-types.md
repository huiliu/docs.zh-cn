---
ms.openlocfilehash: b01424c63d6e7956127bf889c53422b60ba2f219
ms.sourcegitcommit: a69d548f90a03e105ee6701236c38390ecd9ccd1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/14/2020
ms.locfileid: "90065131"
---
### <a name="ca2013-do-not-use-referenceequals-with-value-types"></a>CA2013:请勿将 ReferenceEquals 与值类型结合使用

从 .NET 5.0 开始，默认启用 .NET 代码分析器规则 [CA2013](/visualstudio/code-quality/ca2013)。 对于使用 <xref:System.Object.ReferenceEquals(System.Object,System.Object)> 比较一个或多个值类型的相等性的代码，它会生成任何生成警告。

#### <a name="change-description"></a>更改说明

从 .NET 5.0 开始，.NET SDK 包括 [.NET 源代码分析器](../../../../docs/fundamentals/productivity/code-analysis.md)。 其中一些规则会默认启用，包括 [CA2013](/visualstudio/code-quality/ca2013)。 如果项目包含违反此规则的代码，并已被配置为将警告视为错误，则此更改可能会中断生成。

规则 CA2013 查找使用 <xref:System.Object.ReferenceEquals(System.Object,System.Object)> 比较一个或多个值类型的相等性的实例。 通过此方式比较值类型的相等性可能会导致错误的结果，因为会先限定这些值，然后再将其进行比较。 即使比较的值表示值类型的同一个实例，<xref:System.Object.ReferenceEquals(System.Object,System.Object)> 也会返回 `false`。

#### <a name="version-introduced"></a>引入的版本

5.0 预览版 8

#### <a name="recommended-action"></a>建议操作

- 更改代码以使用适当的相等运算符，例如 `==`。 不应禁止显示此警告。

- 若要完全禁用代码分析，请在项目文件中将 `EnableNETAnalyzers` 设置为 `false`。 有关详细信息，请参阅 [EnableNETAnalyzers](../../../../docs/core/project-sdk/msbuild-props.md#enablenetanalyzers)。

#### <a name="category"></a>类别

代码分析

#### <a name="affected-apis"></a>受影响的 API

- <xref:System.Object.ReferenceEquals(System.Object,System.Object)?displayProperty=fullName>

<!--

#### Affected APIs

- `M:System.Object.ReferenceEquals(System.Object,System.Object)`

-->
