---
title: Celdas de referencia (F#)
description: "Obtenga información acerca de cómo las celdas de referencia de F # son ubicaciones de almacenamiento que le permiten crear valores mutables con semántica de referencias."
keywords: "visual f#, f#, programación funcional"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 09a0b221-ea21-45c4-bae8-5e4a339750c4
ms.openlocfilehash: c7470c9a36cf2cd24dd89ceffcf6e90c6dc4d2dd
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="reference-cells"></a><span data-ttu-id="cfe18-104">Celdas de referencia</span><span class="sxs-lookup"><span data-stu-id="cfe18-104">Reference Cells</span></span>

<span data-ttu-id="cfe18-105">*Hacer referencia a las celdas* son ubicaciones de almacenamiento que le permiten crear valores mutables con semántica de referencias.</span><span class="sxs-lookup"><span data-stu-id="cfe18-105">*Reference cells* are storage locations that enable you to create mutable values with reference semantics.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe18-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfe18-106">Syntax</span></span>

```fsharp
ref expression
```

## <a name="remarks"></a><span data-ttu-id="cfe18-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cfe18-107">Remarks</span></span>
<span data-ttu-id="cfe18-108">Se utiliza el operador `ref` antes de un valor para crear una nueva celda de referencia que encapsula el valor.</span><span class="sxs-lookup"><span data-stu-id="cfe18-108">You use the `ref` operator before a value to create a new reference cell that encapsulates the value.</span></span> <span data-ttu-id="cfe18-109">A continuación, se puede cambiar el valor subyacente, porque es mutable.</span><span class="sxs-lookup"><span data-stu-id="cfe18-109">You can then change the underlying value because it is mutable.</span></span>

<span data-ttu-id="cfe18-110">Una celda de referencia contiene un valor real; no una mera dirección.</span><span class="sxs-lookup"><span data-stu-id="cfe18-110">A reference cell holds an actual value; it is not just an address.</span></span> <span data-ttu-id="cfe18-111">Al crear una celda de referencia mediante el operador `ref`, se crea una copia del valor subyacente como valor mutable encapsulado.</span><span class="sxs-lookup"><span data-stu-id="cfe18-111">When you create a reference cell by using the `ref` operator, you create a copy of the underlying value as an encapsulated mutable value.</span></span>

<span data-ttu-id="cfe18-112">Se puede desreferenciar una celda de referencia mediante el operador `!` (bang).</span><span class="sxs-lookup"><span data-stu-id="cfe18-112">You can dereference a reference cell by using the `!` (bang) operator.</span></span>

<span data-ttu-id="cfe18-113">En el ejemplo de código siguiente se muestran la declaración y el uso de celdas de referencia.</span><span class="sxs-lookup"><span data-stu-id="cfe18-113">The following code example illustrates the declaration and use of reference cells.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2201.fs)]

<span data-ttu-id="cfe18-114">El resultado es `50`</span><span class="sxs-lookup"><span data-stu-id="cfe18-114">The output is `50`.</span></span>

<span data-ttu-id="cfe18-115">Las celdas de referencia son instancias del tipo de registro genérico `Ref`, que se declara como sigue.</span><span class="sxs-lookup"><span data-stu-id="cfe18-115">Reference cells are instances of the `Ref` generic record type, which is declared as follows.</span></span>

```fsharp
type Ref<'a> =
{ mutable contents: 'a }
```

<span data-ttu-id="cfe18-116">El tipo `'a ref` es un sinónimo de `Ref<'a>`.</span><span class="sxs-lookup"><span data-stu-id="cfe18-116">The type `'a ref` is a synonym for `Ref<'a>`.</span></span> <span data-ttu-id="cfe18-117">Tanto el compilador como IntelliSense en el IDE, muestran el primero para este tipo, pero la definición subyacente es el segundo.</span><span class="sxs-lookup"><span data-stu-id="cfe18-117">The compiler and IntelliSense in the IDE display the former for this type, but the underlying definition is the latter.</span></span>

<span data-ttu-id="cfe18-118">El operador `ref` crea una nueva celda de referencia.</span><span class="sxs-lookup"><span data-stu-id="cfe18-118">The `ref` operator creates a new reference cell.</span></span> <span data-ttu-id="cfe18-119">El código siguiente es la declaración del operador `ref`.</span><span class="sxs-lookup"><span data-stu-id="cfe18-119">The following code is the declaration of the `ref` operator.</span></span>

```fsharp
let ref x = { contents = x }
```

<span data-ttu-id="cfe18-120">En la tabla siguiente se muestran las características que están disponibles en la celda de referencia.</span><span class="sxs-lookup"><span data-stu-id="cfe18-120">The following table shows the features that are available on the reference cell.</span></span>

|<span data-ttu-id="cfe18-121">Operador, miembro o campo</span><span class="sxs-lookup"><span data-stu-id="cfe18-121">Operator, member, or field</span></span>|<span data-ttu-id="cfe18-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfe18-122">Description</span></span>|<span data-ttu-id="cfe18-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="cfe18-123">Type</span></span>|<span data-ttu-id="cfe18-124">Definición</span><span class="sxs-lookup"><span data-stu-id="cfe18-124">Definition</span></span>|
|--------------------------|-----------|----|----------|
|<span data-ttu-id="cfe18-125">`!` (operador de desreferencia)</span><span class="sxs-lookup"><span data-stu-id="cfe18-125">`!` (dereference operator)</span></span>|<span data-ttu-id="cfe18-126">Devuelve el valor subyacente.</span><span class="sxs-lookup"><span data-stu-id="cfe18-126">Returns the underlying value.</span></span>|`'a ref -> 'a`|`let (!) r = r.contents`|
|<span data-ttu-id="cfe18-127">`:=` (operador de asignación)</span><span class="sxs-lookup"><span data-stu-id="cfe18-127">`:=` (assignment operator)</span></span>|<span data-ttu-id="cfe18-128">Cambia el valor subyacente.</span><span class="sxs-lookup"><span data-stu-id="cfe18-128">Changes the underlying value.</span></span>|`'a ref -> 'a -> unit`|`let (:=) r x = r.contents <- x`|
|<span data-ttu-id="cfe18-129">`ref` (operador)</span><span class="sxs-lookup"><span data-stu-id="cfe18-129">`ref` (operator)</span></span>|<span data-ttu-id="cfe18-130">Encapsula un valor en una nueva celda de referencia.</span><span class="sxs-lookup"><span data-stu-id="cfe18-130">Encapsulates a value into a new reference cell.</span></span>|`'a -> 'a ref`|`let ref x = { contents = x }`|
|<span data-ttu-id="cfe18-131">`Value` (propiedad)</span><span class="sxs-lookup"><span data-stu-id="cfe18-131">`Value` (property)</span></span>|<span data-ttu-id="cfe18-132">Obtiene o establece el valor subyacente.</span><span class="sxs-lookup"><span data-stu-id="cfe18-132">Gets or sets the underlying value.</span></span>|`unit -> 'a`|`member x.Value = x.contents`|
|<span data-ttu-id="cfe18-133">`contents` (campo de registro)</span><span class="sxs-lookup"><span data-stu-id="cfe18-133">`contents` (record field)</span></span>|<span data-ttu-id="cfe18-134">Obtiene o establece el valor subyacente.</span><span class="sxs-lookup"><span data-stu-id="cfe18-134">Gets or sets the underlying value.</span></span>|`'a`|`let ref x = { contents = x }`|
<span data-ttu-id="cfe18-135">Hay varias maneras de tener acceso al valor subyacente.</span><span class="sxs-lookup"><span data-stu-id="cfe18-135">There are several ways to access the underlying value.</span></span> <span data-ttu-id="cfe18-136">El valor devuelto por el operador de desreferencia (`!`) no es un valor asignable.</span><span class="sxs-lookup"><span data-stu-id="cfe18-136">The value returned by the dereference operator (`!`) is not an assignable value.</span></span> <span data-ttu-id="cfe18-137">Por consiguiente, si se va a modificar el valor subyacente, se debe utilizar el operador de asignación (`:=`) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="cfe18-137">Therefore, if you are modifying the underlying value, you must use the assignment operator (`:=`) instead.</span></span>

<span data-ttu-id="cfe18-138">Tanto la propiedad `Value` como el campo `contents` son valores asignables.</span><span class="sxs-lookup"><span data-stu-id="cfe18-138">Both the `Value` property and the `contents` field are assignable values.</span></span> <span data-ttu-id="cfe18-139">Así pues, se pueden utilizar para obtener acceso al valor subyacente o cambiarlo, como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="cfe18-139">Therefore, you can use these to either access or change the underlying value, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2203.fs)]

<span data-ttu-id="cfe18-140">La salida es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="cfe18-140">The output is as follows.</span></span>

```
10
10
11
12
```

<span data-ttu-id="cfe18-141">El campo `contents` se proporciona por motivos de compatibilidad con otras versiones de ML y generará una advertencia durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="cfe18-141">The field `contents` is provided for compatibility with other versions of ML and will produce a warning during compilation.</span></span> <span data-ttu-id="cfe18-142">Para deshabilitar la advertencia, utilice la opción `--mlcompatibility` del compilador.</span><span class="sxs-lookup"><span data-stu-id="cfe18-142">To disable the warning, use the `--mlcompatibility` compiler option.</span></span> <span data-ttu-id="cfe18-143">Para obtener más información, consulte [Opciones del compilador](compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="cfe18-143">For more information, see [Compiler Options](compiler-options.md).</span></span>

<span data-ttu-id="cfe18-144">El código siguiente muestra el uso de celdas de referencia al pasar parámetros.</span><span class="sxs-lookup"><span data-stu-id="cfe18-144">The following code illustrates the use of reference cells in parameter passing.</span></span> <span data-ttu-id="cfe18-145">El tipo de Incrementor tiene un método Increment que toma un parámetro que incluye byref en el tipo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="cfe18-145">The Incrementor type has a method Increment that takes a parameter that includes byref in the parameter type.</span></span> <span data-ttu-id="cfe18-146">Byref en el tipo de parámetro indica que los llamadores deben pasar una celda de referencia o la dirección de una variable típica del tipo especificado, en este caso int El resto del código muestra cómo llamar a incremento con ambos tipos de argumentos y muestra el uso del operador ref en una variable para crear una celda de referencia (ref myDelta1).</span><span class="sxs-lookup"><span data-stu-id="cfe18-146">The byref in the parameter type indicates that callers must pass a reference cell or the address of a typical variable of the specified type, in this case int. The remaining code illustrates how to call Increment with both of these types of arguments, and shows the use of the ref operator on a variable to create a reference cell (ref myDelta1).</span></span> <span data-ttu-id="cfe18-147">A continuación, se muestra el uso del operador de dirección de (&amp;) para generar un argumento adecuado.</span><span class="sxs-lookup"><span data-stu-id="cfe18-147">It then shows the use of the address-of operator (&amp;) to generate an appropriate argument.</span></span> <span data-ttu-id="cfe18-148">Por último, el método Increment se llama de nuevo mediante el uso de una celda de referencia que se declara mediante un enlace let.</span><span class="sxs-lookup"><span data-stu-id="cfe18-148">Finally, the Increment method is called again by using a reference cell that is declared by using a let binding.</span></span> <span data-ttu-id="cfe18-149">La última línea del código muestra el uso de la!</span><span class="sxs-lookup"><span data-stu-id="cfe18-149">The final line of code demonstrates the use of the !</span></span> <span data-ttu-id="cfe18-150">operador a fin de desreferenciar la celda de referencia para su impresión.</span><span class="sxs-lookup"><span data-stu-id="cfe18-150">operator to dereference the reference cell for printing.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2204.fs)]

<span data-ttu-id="cfe18-151">Para obtener más información sobre cómo pasar por referencia, vea [parámetros y argumentos](parameters-and-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="cfe18-151">For more information about how to pass by reference, see [Parameters and Arguments](parameters-and-arguments.md).</span></span>

>[!NOTE]
<span data-ttu-id="cfe18-152">Programadores de C# deben saber que ref funciona forma distinta en F # que en C#.</span><span class="sxs-lookup"><span data-stu-id="cfe18-152">C# programmers should know that ref works differently in F# than it does in C#.</span></span> <span data-ttu-id="cfe18-153">Por ejemplo, el uso de ref cuando se pasa un argumento no tiene el mismo efecto en F # como ocurre en C#.</span><span class="sxs-lookup"><span data-stu-id="cfe18-153">For example, the use of ref when you pass an argument does not have the same effect in F# as it does in C#.</span></span>

## <a name="consuming-c-ref-returns"></a><span data-ttu-id="cfe18-154">Utilizar en C# `ref` devuelve</span><span class="sxs-lookup"><span data-stu-id="cfe18-154">Consuming C# `ref` returns</span></span>

<span data-ttu-id="cfe18-155">A partir de F # 4.1, puedes utilizar `ref` devuelve generado en C#.</span><span class="sxs-lookup"><span data-stu-id="cfe18-155">Starting with F# 4.1, you can consume `ref` returns generated in C#.</span></span>  <span data-ttu-id="cfe18-156">El resultado de una llamada de este tipo es un `byref<_>` puntero.</span><span class="sxs-lookup"><span data-stu-id="cfe18-156">The result of such a call is a `byref<_>` pointer.</span></span>

<span data-ttu-id="cfe18-157">El siguiente método de C#:</span><span class="sxs-lookup"><span data-stu-id="cfe18-157">The following C# method:</span></span>

```csharp
namespace RefReturns
{
    public static class RefClass
    {
        public static ref int Find(int val, int[] vals)
        {
            for (int i = 0; i < vals.Length; i++)
            {
                if (vals[i] == val)
                {
                    return ref numbers[i]; // Returns the location, not the value
                }
            }

            throw new IndexOutOfRangeException($"{nameof(number)} not found");
        }
    }
}
```

<span data-ttu-id="cfe18-158">Puede ser transparente llama F # con ninguna sintaxis especial:</span><span class="sxs-lookup"><span data-stu-id="cfe18-158">Can be transparently called by F# with no special syntax:</span></span>

```fsharp
open RefReturns

let consumeRefReturn() =
    let result = RefClass.Find(3, [| 1; 2; 3; 4; 5 |]) // 'result' is of type 'byref<int>'.
    ()
```

<span data-ttu-id="cfe18-159">También puede declarar funciones que pueden durar un `ref` devolver como entrada, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cfe18-159">You can also declare functions which could take a `ref` return as input, for example:</span></span>

```fsharp
let f (x: byref<int>) = &x
```

<span data-ttu-id="cfe18-160">Actualmente no hay ninguna manera de generar un `ref` devuelto en F # que en C# que pueden consumir.</span><span class="sxs-lookup"><span data-stu-id="cfe18-160">There is currently no way to generate a `ref` return in F# which could be consumed in C#.</span></span>

## <a name="see-also"></a><span data-ttu-id="cfe18-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfe18-161">See Also</span></span>
[<span data-ttu-id="cfe18-162">Referencia del lenguaje F#</span><span class="sxs-lookup"><span data-stu-id="cfe18-162">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="cfe18-163">Parámetros y argumentos</span><span class="sxs-lookup"><span data-stu-id="cfe18-163">Parameters and Arguments</span></span>](parameters-and-arguments.md)

[<span data-ttu-id="cfe18-164">Referencia de símbolos y operadores</span><span class="sxs-lookup"><span data-stu-id="cfe18-164">Symbol and Operator Reference</span></span>](symbol-and-operator-reference/index.md)