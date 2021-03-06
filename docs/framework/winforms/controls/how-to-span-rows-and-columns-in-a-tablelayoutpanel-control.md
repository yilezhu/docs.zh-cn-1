---
title: 如何：在 TableLayoutPanel 控件中跨行和跨列
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.SpanRowsColumns
helpviewer_keywords:
- columns [Windows Forms], spanning
- merging cells
- TableLayoutPanel control [Windows Forms], spanning rows and columns
- rows [Windows Forms], spanning
- cells [Windows Forms], merging
ms.assetid: a8a2fdd3-a848-48b0-a4cd-4e85ebded87e
ms.openlocfilehash: 02db78b07930676235e55e535fb24f6ff618d823
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59339016"
---
# <a name="how-to-span-rows-and-columns-in-a-tablelayoutpanel-control"></a>如何：在 TableLayoutPanel 控件中跨行和跨列
中的控件<xref:System.Windows.Forms.TableLayoutPanel>控件可以跨越相邻的行和列。  
  
> [!NOTE]
>  显示的对话框和菜单命令可能会与“帮助”中的描述不同，具体取决于你现用的设置或版本。 若要更改设置，请在 **“工具”** 菜单上选择 **“导入和导出设置”** 。 有关详细信息，请参阅[个性化设置 Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide)。  
  
### <a name="to-span-columns-and-rows"></a>若要跨的列和行  
  
1. 从 <xref:System.Windows.Forms.TableLayoutPanel> “工具箱” **将** 控件拖到你的窗体上。  
  
2. 拖动<xref:System.Windows.Forms.Button>控件从**工具箱**到的左上角单元格<xref:System.Windows.Forms.TableLayoutPanel>控件。  
  
3. 设置<xref:System.Windows.Forms.Button>控件的**ColumnSpan**属性设置为**2**。 请注意，<xref:System.Windows.Forms.Button>控件跨的第一个和第二个列。  
  
4. 设置<xref:System.Windows.Forms.Button>控件的**RowSpan**属性设置为**2**。 请注意，<xref:System.Windows.Forms.Button>控件跨的第一个和第二个行。  
  
5. 设置<xref:System.Windows.Forms.Button>控件的**ColumnSpan**属性设置为**1**。 请注意，<xref:System.Windows.Forms.Button>控件将移动到第一列并跨越的第一个和第二个行。  
  
## <a name="see-also"></a>请参阅

- [TableLayoutPanel 控件](tablelayoutpanel-control-windows-forms.md)
