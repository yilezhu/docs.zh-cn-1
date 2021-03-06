---
title: 如何：在运行时从 PrintDialog 中捕获用户输入
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- print options [Windows Forms], changing at run time
- printing [Windows Forms], options
- print options
- run time [Windows Forms], changing print options
ms.assetid: 438501d8-9a70-4fb3-aae6-e46579aba0c6
ms.openlocfilehash: 2aaf988f362baf9cd80eb16e4a08f7f65a5077bb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59311417"
---
# <a name="how-to-capture-user-input-from-a-printdialog-at-run-time"></a>如何：在运行时从 PrintDialog 中捕获用户输入
虽然您可以设置与在设计时打印相关的选项，有时想要在运行时，最有可能由于所做的用户选择更改这些选项。 您可以捕获用于打印文档中使用的用户输入<xref:System.Windows.Forms.PrintDialog>和<xref:System.Drawing.Printing.PrintDocument>组件。  
  
### <a name="to-change-print-options-programmatically"></a>若要以编程方式更改打印选项  
  
1. 添加<xref:System.Windows.Forms.PrintDialog>和一个<xref:System.Drawing.Printing.PrintDocument>向窗体组件。  
  
2. 设置<xref:System.Windows.Forms.PrintDialog.Document%2A>的属性<xref:System.Windows.Forms.PrintDialog>到<xref:System.Drawing.Printing.PrintDocument>添加到窗体。  
  
    ```vb  
    PrintDialog1.Document = PrintDocument1  
    ```  
  
    ```csharp  
    printDialog1.Document = PrintDocument1;  
    ```  
  
    ```cpp  
    printDialog1->Document = PrintDocument1;  
    ```  
  
3. 显示<xref:System.Windows.Forms.PrintDialog>组件使用<xref:System.Windows.Forms.CommonDialog.ShowDialog%2A>方法。  
  
    ```vb  
    PrintDialog1.ShowDialog()  
    ```  
  
    ```csharp  
    printDialog1.ShowDialog();  
    ```  
  
    ```cpp  
    printDialog1->ShowDialog();  
    ```  
  
4. 在对话框中的用户的打印选项将被复制到<xref:System.Drawing.Printing.PrinterSettings>属性的<xref:System.Drawing.Printing.PrintDocument>组件。  
  
## <a name="see-also"></a>请参阅

- [如何：打印 Windows 窗体中的多页文本文件](how-to-print-a-multi-page-text-file-in-windows-forms.md)
- [Windows 窗体打印支持](windows-forms-print-support.md)
