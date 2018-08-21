---
title: 'Tipos básicos (F #)'
description: 'Descubra los tipos básicos fundamentales que se usan en el lenguaje F #.'
ms.date: 07/09/2018
ms.openlocfilehash: fdb5e95e102fcf721569156c7fb3a32604fff1dd
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/10/2018
ms.locfileid: "37937202"
---
# <a name="basic-types"></a><span data-ttu-id="ae322-103">Tipos básicos</span><span class="sxs-lookup"><span data-stu-id="ae322-103">Basic types</span></span>

<span data-ttu-id="ae322-104">En este tema se enumera los tipos básicos que se definen en el lenguaje F #.</span><span class="sxs-lookup"><span data-stu-id="ae322-104">This topic lists the basic types that are defined in the F# language.</span></span> <span data-ttu-id="ae322-105">Estos tipos son más importantes en F #, que forman la base de casi todos los programas F #.</span><span class="sxs-lookup"><span data-stu-id="ae322-105">These types are the most fundamental in F#, forming the basis of nearly every F# program.</span></span> <span data-ttu-id="ae322-106">Son un superconjunto de los tipos primitivos. NET.</span><span class="sxs-lookup"><span data-stu-id="ae322-106">They are a superset of .NET primitive types.</span></span>

|<span data-ttu-id="ae322-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae322-107">Type</span></span>|<span data-ttu-id="ae322-108">Tipo de .NET</span><span class="sxs-lookup"><span data-stu-id="ae322-108">.NET type</span></span>|<span data-ttu-id="ae322-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae322-109">Description</span></span>|
|----|---------|-----------|
|`bool`|<xref:System.Boolean>|<span data-ttu-id="ae322-110">Los valores posibles son `true` y `false`.</span><span class="sxs-lookup"><span data-stu-id="ae322-110">Possible values are `true` and `false`.</span></span>|
|`byte`|<xref:System.Byte>|<span data-ttu-id="ae322-111">Valores de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="ae322-111">Values from 0 to 255.</span></span>|
|`sbyte`|<xref:System.SByte>|<span data-ttu-id="ae322-112">Valores de -128 a 127.</span><span class="sxs-lookup"><span data-stu-id="ae322-112">Values from -128 to 127.</span></span>|
|`int16`|<xref:System.Int16>|<span data-ttu-id="ae322-113">Valores de -32768 a 32767.</span><span class="sxs-lookup"><span data-stu-id="ae322-113">Values from -32768 to 32767.</span></span>|
|`uint16`|<xref:System.UInt16>|<span data-ttu-id="ae322-114">Valores de 0 a 65535.</span><span class="sxs-lookup"><span data-stu-id="ae322-114">Values from 0 to 65535.</span></span>|
|`int`|<xref:System.Int32>|<span data-ttu-id="ae322-115">Valores entre -2.147.483.648 a 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="ae322-115">Values from -2,147,483,648 to 2,147,483,647.</span></span>|
|`uint32`|<xref:System.UInt32>|<span data-ttu-id="ae322-116">Valores entre 0 y 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="ae322-116">Values from 0 to 4,294,967,295.</span></span>|
|`int64`|<xref:System.Int64>|<span data-ttu-id="ae322-117">Valores comprendidos entre -9.223.372.036.854.775.808 a + 9.223.372.036.854.775.807.</span><span class="sxs-lookup"><span data-stu-id="ae322-117">Values from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.</span></span>|
|`uint64`|<xref:System.UInt64>|<span data-ttu-id="ae322-118">Valores de 0 a 18,446,744,073,709,551,615.</span><span class="sxs-lookup"><span data-stu-id="ae322-118">Values from 0 to 18,446,744,073,709,551,615.</span></span>|
|`nativeint`|<xref:System.IntPtr>|<span data-ttu-id="ae322-119">Un puntero nativo como un entero con signo.</span><span class="sxs-lookup"><span data-stu-id="ae322-119">A native pointer as a signed integer.</span></span>|
|`unativeint`|<xref:System.UIntPtr>|<span data-ttu-id="ae322-120">Un puntero nativo como un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="ae322-120">A native pointer as an unsigned integer.</span></span>|
|`char`|<xref:System.Char>|<span data-ttu-id="ae322-121">Valores de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae322-121">Unicode character values.</span></span>|
|`string`|<xref:System.String>|<span data-ttu-id="ae322-122">Texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae322-122">Unicode text.</span></span>|
|`decimal`|<xref:System.Decimal>|<span data-ttu-id="ae322-123">Tipo de datos que tiene al menos 28 dígitos significativos de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="ae322-123">A floating point data type that has at least 28 significant digits.</span></span>|
|`unit`|<span data-ttu-id="ae322-124">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ae322-124">not applicable</span></span>|<span data-ttu-id="ae322-125">Indica la ausencia de un valor real.</span><span class="sxs-lookup"><span data-stu-id="ae322-125">Indicates the absence of an actual value.</span></span> <span data-ttu-id="ae322-126">El tipo tiene un único valor formal, que se indica `()`.</span><span class="sxs-lookup"><span data-stu-id="ae322-126">The type has only one formal value, which is denoted `()`.</span></span> <span data-ttu-id="ae322-127">El valor de unidad, `()`, a menudo se usa como marcador de posición donde se necesita un valor pero ningún valor real está disponible o que tenga sentido.</span><span class="sxs-lookup"><span data-stu-id="ae322-127">The unit value, `()`, is often used as a placeholder where a value is needed but no real value is available or makes sense.</span></span>|
|`void`|<xref:System.Void>|<span data-ttu-id="ae322-128">No indica que ningún tipo de valor.</span><span class="sxs-lookup"><span data-stu-id="ae322-128">Indicates no type or value.</span></span>|
|<span data-ttu-id="ae322-129">`float32`, `single`</span><span class="sxs-lookup"><span data-stu-id="ae322-129">`float32`, `single`</span></span>|<xref:System.Single>|<span data-ttu-id="ae322-130">Tipo de punto flotante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ae322-130">A 32-bit floating point type.</span></span>|
|<span data-ttu-id="ae322-131">`float`, `double`</span><span class="sxs-lookup"><span data-stu-id="ae322-131">`float`, `double`</span></span>|<xref:System.Double>|<span data-ttu-id="ae322-132">Tipo de punto flotante de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ae322-132">A 64-bit floating point type.</span></span>|

>[!NOTE]
<span data-ttu-id="ae322-133">Puede realizar cálculos con números enteros demasiado grandes para el tipo de entero de 64 bits mediante el [bigint](https://msdn.microsoft.com/library/dc8be18d-4042-46c4-b136-2f21a84f6efa) tipo.</span><span class="sxs-lookup"><span data-stu-id="ae322-133">You can perform computations with integers too big for the 64-bit integer type by using the [bigint](https://msdn.microsoft.com/library/dc8be18d-4042-46c4-b136-2f21a84f6efa) type.</span></span> <span data-ttu-id="ae322-134">`bigint` no se considera un tipo básico; es la abreviatura de `System.Numerics.BigInteger`.</span><span class="sxs-lookup"><span data-stu-id="ae322-134">`bigint` is not considered a basic type; it is an abbreviation for `System.Numerics.BigInteger`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae322-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae322-135">See also</span></span>
[<span data-ttu-id="ae322-136">Referencia del lenguaje F#</span><span class="sxs-lookup"><span data-stu-id="ae322-136">F# Language Reference</span></span>](index.md)