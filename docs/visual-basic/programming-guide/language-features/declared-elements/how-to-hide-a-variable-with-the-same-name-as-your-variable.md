---
title: "Nasıl yapılır: Değişkeninizle Aynı Adı Taşıyan Bir Değişkeni Gizleme (Visual Basic)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- qualification [Visual Basic], of element names
- declarations [Visual Basic], elements
- element names [Visual Basic], qualification
- references [Visual Basic], declared elements
- declaration statements [Visual Basic], declared elements
- declaring elements [Visual Basic]
- referencing declared elements [Visual Basic]
- declared elements [Visual Basic], referencing
- declared elements [Visual Basic], about declared elements
ms.assetid: e39c0752-f19f-4d2e-a453-00df1b5fc7ee
caps.latest.revision: "25"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: af031f3ef134b2a509922e6ada28aa5b2b80d641
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-hide-a-variable-with-the-same-name-as-your-variable-visual-basic"></a><span data-ttu-id="d308c-102">Nasıl yapılır: Değişkeninizle Aynı Adı Taşıyan Bir Değişkeni Gizleme (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d308c-102">How to: Hide a Variable with the Same Name as Your Variable (Visual Basic)</span></span>
<span data-ttu-id="d308c-103">Bir değişkenin gizleyebilirsiniz *gölgeleme* , diğer bir deyişle, aynı ada sahip bir değişken tanımlayarak tarafından.</span><span class="sxs-lookup"><span data-stu-id="d308c-103">You can hide a variable by *shadowing* it, that is, by redefining it with a variable of the same name.</span></span> <span data-ttu-id="d308c-104">İki yolla gizlemek istediğiniz değişkeni gölge:</span><span class="sxs-lookup"><span data-stu-id="d308c-104">You can shadow the variable you want to hide in two ways:</span></span>  
  
-   <span data-ttu-id="d308c-105">**Kapsam yoluyla gölgeleme.**</span><span class="sxs-lookup"><span data-stu-id="d308c-105">**Shadowing Through Scope.**</span></span> <span data-ttu-id="d308c-106">Bu kapsam yoluyla gizlemek istediğiniz değişkenini içeren bölgenin alt içinde redeclaring tarafından gölge.</span><span class="sxs-lookup"><span data-stu-id="d308c-106">You can shadow it through scope by redeclaring it inside a subregion of the region containing the variable you want to hide.</span></span>  
  
-   <span data-ttu-id="d308c-107">**Devralma yoluyla gölgeleme.**</span><span class="sxs-lookup"><span data-stu-id="d308c-107">**Shadowing Through Inheritance.**</span></span> <span data-ttu-id="d308c-108">Gizlemek istediğiniz değişken sınıf düzeyinde tanımlanmışsa, bu devralma yoluyla ile redeclaring gölge [gölgeleri](../../../../visual-basic/language-reference/modifiers/shadows.md) türetilmiş bir sınıf bir anahtar sözcük.</span><span class="sxs-lookup"><span data-stu-id="d308c-108">If the variable you want to hide is defined at class level, you can shadow it through inheritance by redeclaring it with the [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md) keyword in a derived class.</span></span>  
  
## <a name="two-ways-to-hide-a-variable"></a><span data-ttu-id="d308c-109">Bir değişkeni gizleme için iki yol</span><span class="sxs-lookup"><span data-stu-id="d308c-109">Two Ways to Hide a Variable</span></span>  
  
#### <a name="to-hide-a-variable-by-shadowing-it-through-scope"></a><span data-ttu-id="d308c-110">Kapsam yoluyla gölgeleme tarafından bir değişkeni gizleme</span><span class="sxs-lookup"><span data-stu-id="d308c-110">To hide a variable by shadowing it through scope</span></span>  
  
1.  <span data-ttu-id="d308c-111">Gizlemek istediğiniz değişken tanımlama bölge belirlemek ve bir alt bölgeli değişkeni ile yeniden tanımlamak üzere belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d308c-111">Determine the region defining the variable you want to hide, and determine a subregion in which to redefine it with your variable.</span></span>  
  
    |<span data-ttu-id="d308c-112">Değişkenin bölge</span><span class="sxs-lookup"><span data-stu-id="d308c-112">Variable's region</span></span>|<span data-ttu-id="d308c-113">Bunu yeniden tanımlama için izin verilen alt</span><span class="sxs-lookup"><span data-stu-id="d308c-113">Allowable subregion for redefining it</span></span>|  
    |-----------------------|-------------------------------------------|  
    |<span data-ttu-id="d308c-114">Modül</span><span class="sxs-lookup"><span data-stu-id="d308c-114">Module</span></span>|<span data-ttu-id="d308c-115">Modüldeki bir sınıfı</span><span class="sxs-lookup"><span data-stu-id="d308c-115">A class within the module</span></span>|  
    |<span data-ttu-id="d308c-116">örneği</span><span class="sxs-lookup"><span data-stu-id="d308c-116">Class</span></span>|<span data-ttu-id="d308c-117">İçindeki bir alt sınıfı</span><span class="sxs-lookup"><span data-stu-id="d308c-117">A subclass within the class</span></span><br /><br /> <span data-ttu-id="d308c-118">Bir yordam içinde sınıfı</span><span class="sxs-lookup"><span data-stu-id="d308c-118">A procedure within the class</span></span>|  
  
     <span data-ttu-id="d308c-119">Bu yordamı blokta yordamı değişkeninde örneğin içinde tanımlanamaz bir `If`... `End If` yapım veya `For` döngü.</span><span class="sxs-lookup"><span data-stu-id="d308c-119">You cannot redefine a procedure variable in a block within that procedure, for example in an `If`...`End If` construction or a `For` loop.</span></span>  
  
2.  <span data-ttu-id="d308c-120">Zaten yoksa, alt bölge oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d308c-120">Create the subregion if it does not already exist.</span></span>  
  
3.  <span data-ttu-id="d308c-121">Alt bölge içinde yazma bir [Dim deyimi](../../../../visual-basic/language-reference/statements/dim-statement.md) gölgeleme değişken bildirme.</span><span class="sxs-lookup"><span data-stu-id="d308c-121">Within the subregion, write a [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md) declaring the shadowing variable.</span></span>  
  
     <span data-ttu-id="d308c-122">Alt bölge içinde kod değişken adına başvurduğunda derleyici gölgeleme değişkeni referansı çözümler.</span><span class="sxs-lookup"><span data-stu-id="d308c-122">When code inside the subregion refers to the variable name, the compiler resolves the reference to the shadowing variable.</span></span>  
  
     <span data-ttu-id="d308c-123">Aşağıdaki örnek, kapsam olarak gölgeleme atlayan bir başvuru gölgeleme gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d308c-123">The following example illustrates shadowing through scope, as well as a reference that bypasses the shadowing.</span></span>  
  
    ```  
    Module shadowByScope  
        ' The following statement declares num as a module-level variable.  
        Public num As Integer  
        Sub show()  
            ' The following statement declares num as a local variable.  
            Dim num As Integer  
            ' The following statement sets the value of the local variable.  
            num = 2  
            ' The following statement displays the module-level variable.  
            MsgBox(CStr(shadowByScope.num))  
        End Sub  
        Sub useModuleLevelNum()  
            ' The following statement sets the value of the module-level variable.  
            num = 1  
            show()  
        End Sub  
    End Module  
    ```  
  
     <span data-ttu-id="d308c-124">Önceki örnekte değişken bildirir `num` hem modül düzeyi ve yordam düzeyinde (yordamda `show`).</span><span class="sxs-lookup"><span data-stu-id="d308c-124">The preceding example declares the variable `num` both at module level and at procedure level (in the procedure `show`).</span></span> <span data-ttu-id="d308c-125">Yerel değişken `num` modül düzeyi değişkeni shadows `num` içinde `show`, yerel değişken 2'ye ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d308c-125">The local variable `num` shadows the module-level variable `num` within `show`, so the local variable is set to 2.</span></span> <span data-ttu-id="d308c-126">Ancak, hiçbir yerel bir gölge değişkene yoktur `num` içinde `useModuleLevelNum` yordamı.</span><span class="sxs-lookup"><span data-stu-id="d308c-126">However, there is no local variable to shadow `num` in the `useModuleLevelNum` procedure.</span></span> <span data-ttu-id="d308c-127">Bu nedenle, `useModuleLevelNum` modül düzeyi değişkenin değerini 1 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d308c-127">Therefore, `useModuleLevelNum` sets the value of the module-level variable to 1.</span></span>  
  
     <span data-ttu-id="d308c-128">`MsgBox` İçinde arama `show` niteleme tarafından gölgeleme mekanizması atlar `num` modül adına sahip.</span><span class="sxs-lookup"><span data-stu-id="d308c-128">The `MsgBox` call inside `show` bypasses the shadowing mechanism by qualifying `num` with the module name.</span></span> <span data-ttu-id="d308c-129">Bu nedenle, yerel değişken yerine modül düzeyi değişkeni görüntüler.</span><span class="sxs-lookup"><span data-stu-id="d308c-129">Therefore, it displays the module-level variable instead of the local variable.</span></span>  
  
#### <a name="to-hide-a-variable-by-shadowing-it-through-inheritance"></a><span data-ttu-id="d308c-130">Devralma yoluyla gölgeleme tarafından bir değişkeni gizleme</span><span class="sxs-lookup"><span data-stu-id="d308c-130">To hide a variable by shadowing it through inheritance</span></span>  
  
1.  <span data-ttu-id="d308c-131">Gizlemek istediğiniz değişkeni bir sınıf ve sınıf düzeyinde (dışında herhangi bir yordam) bildirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="d308c-131">Be sure the variable you want to hide is declared in a class, and at class level (outside any procedure).</span></span> <span data-ttu-id="d308c-132">Aksi takdirde devralma yoluyla gölge olamaz.</span><span class="sxs-lookup"><span data-stu-id="d308c-132">Otherwise you cannot shadow it through inheritance.</span></span>  
  
2.  <span data-ttu-id="d308c-133">Bir zaten yoksa, değişkenin sınıfından türetilen bir sınıfı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d308c-133">Define a class derived from the variable's class if one does not already exist.</span></span>  
  
3.  <span data-ttu-id="d308c-134">Türetilmiş sınıf içinde yazma bir `Dim` deyimi, değişken bildirme.</span><span class="sxs-lookup"><span data-stu-id="d308c-134">Inside the derived class, write a `Dim` statement declaring your variable.</span></span> <span data-ttu-id="d308c-135">Dahil [gölgeleri](../../../../visual-basic/language-reference/modifiers/shadows.md) bildiriminde anahtar sözcüğü.</span><span class="sxs-lookup"><span data-stu-id="d308c-135">Include the [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md) keyword in the declaration.</span></span>  
  
     <span data-ttu-id="d308c-136">Türetilmiş sınıf kodda değişken adına başvurduğunda, derleyici, değişkeni referansı çözümler.</span><span class="sxs-lookup"><span data-stu-id="d308c-136">When code in the derived class refers to the variable name, the compiler resolves the reference to your variable.</span></span>  
  
     <span data-ttu-id="d308c-137">Aşağıdaki örnek, devralma yoluyla gölgeleme gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d308c-137">The following example illustrates shadowing through inheritance.</span></span> <span data-ttu-id="d308c-138">İki başvuru, gölgeleme değişkeni erişen diğeri gölgeleme atlayan kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="d308c-138">It makes two references, one that accesses the shadowing variable and one that bypasses the shadowing.</span></span>  
  
    ```  
    Public Class shadowBaseClass  
        Public shadowString As String = "This is the base class string."  
    End Class  
    Public Class shadowDerivedClass  
        Inherits shadowBaseClass  
        Public Shadows shadowString As String = "This is the derived class string."  
        Public Sub showStrings()  
            Dim s As String = "Unqualified shadowString: " & shadowString &  
                 vbCrLf & "MyBase.shadowString: " & MyBase.shadowString  
            MsgBox(s)  
        End Sub  
    End Class  
    ```  
  
     <span data-ttu-id="d308c-139">Önceki örnekte değişken bildirir `shadowString` temel sınıf ve türetilen sınıfta shadows.</span><span class="sxs-lookup"><span data-stu-id="d308c-139">The preceding example declares the variable `shadowString` in the base class and shadows it in the derived class.</span></span> <span data-ttu-id="d308c-140">Yordamı `showStrings` türetilen sınıfta dize gölgeleme sürümünü görüntüler zaman adı `shadowString` yetkili değil.</span><span class="sxs-lookup"><span data-stu-id="d308c-140">The procedure `showStrings` in the derived class displays the shadowing version of the string when the name `shadowString` is not qualified.</span></span> <span data-ttu-id="d308c-141">Ardından gölgeli sürümünü görüntüler zaman `shadowString` ile nitelenmiş `MyBase` anahtar sözcüğü.</span><span class="sxs-lookup"><span data-stu-id="d308c-141">It then displays the shadowed version when `shadowString` is qualified with the `MyBase` keyword.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="d308c-142">Güçlü Programlama</span><span class="sxs-lookup"><span data-stu-id="d308c-142">Robust Programming</span></span>  
 <span data-ttu-id="d308c-143">Gölgeleme aynı ada sahip bir değişken birden fazla sürümünü getirmektedir.</span><span class="sxs-lookup"><span data-stu-id="d308c-143">Shadowing introduces more than one version of a variable with the same name.</span></span> <span data-ttu-id="d308c-144">Kod açıklaması değişken adına başvurduğunda, derleyici Başvurusu Güvenlik giderir sürüm kod açıklaması konumunu ve uygun bir dize varlığını gibi etkenlere bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d308c-144">When a code statement refers to the variable name, the version to which the compiler resolves the reference depends on factors such as the location of the code statement and the presence of a qualifying string.</span></span> <span data-ttu-id="d308c-145">Bu gölgeli bir değişken istenmeyen bir sürümüne başvuran riskini artırabilir.</span><span class="sxs-lookup"><span data-stu-id="d308c-145">This can increase the risk of referring to an unintended version of a shadowed variable.</span></span> <span data-ttu-id="d308c-146">Bu riski tam olarak gölgeli bir değişken yapılan tüm başvuruları niteleme tarafından düşürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d308c-146">You can lower that risk by fully qualifying all references to a shadowed variable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d308c-147">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="d308c-147">See Also</span></span>  
 [<span data-ttu-id="d308c-148">Bildirilmiş öğelere başvurular</span><span class="sxs-lookup"><span data-stu-id="d308c-148">References to Declared Elements</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)  
 [<span data-ttu-id="d308c-149">Visual Basic'de gölgeleme</span><span class="sxs-lookup"><span data-stu-id="d308c-149">Shadowing in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)  
 [<span data-ttu-id="d308c-150">Gölgeleme ve geçersiz kılma arasındaki farklar</span><span class="sxs-lookup"><span data-stu-id="d308c-150">Differences Between Shadowing and Overriding</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/differences-between-shadowing-and-overriding.md)  
 [<span data-ttu-id="d308c-151">Nasıl yapılır: devralınmış değişkeni gizleme</span><span class="sxs-lookup"><span data-stu-id="d308c-151">How to: Hide an Inherited Variable</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-hide-an-inherited-variable.md)  
 [<span data-ttu-id="d308c-152">Nasıl yapılır: türetilmiş sınıf tarafından gizlenen bir değişkene erişme</span><span class="sxs-lookup"><span data-stu-id="d308c-152">How to: Access a Variable Hidden by a Derived Class</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-access-a-variable-hidden-by-a-derived-class.md)  
 [<span data-ttu-id="d308c-153">Geçersiz kılmaları</span><span class="sxs-lookup"><span data-stu-id="d308c-153">Overrides</span></span>](../../../../visual-basic/language-reference/modifiers/overrides.md)  
 [<span data-ttu-id="d308c-154">Me, My, MyBase ve MyClass</span><span class="sxs-lookup"><span data-stu-id="d308c-154">Me, My, MyBase, and MyClass</span></span>](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)  
 [<span data-ttu-id="d308c-155">Devralma temelleri</span><span class="sxs-lookup"><span data-stu-id="d308c-155">Inheritance Basics</span></span>](../../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)