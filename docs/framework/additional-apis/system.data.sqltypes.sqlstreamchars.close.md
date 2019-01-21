---
title: Método SqlStreamChars.Close (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Close
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 5b7ba05b0659bfd2cad165826469c0c8f0674797
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "54221172"
---
# <a name="sqlstreamcharsclose-method"></a><span data-ttu-id="32b9c-102">Método SqlStreamChars.Close</span><span class="sxs-lookup"><span data-stu-id="32b9c-102">SqlStreamChars.Close Method</span></span>

<span data-ttu-id="32b9c-103">Cierra la secuencia actual y libera los recursos del sistema asociados a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="32b9c-103">Closes the current stream and releases any system resources associated with the stream.</span></span> <span data-ttu-id="32b9c-104">El ensamblado que contiene este método tiene una relación de confianza con SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="32b9c-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="32b9c-105">Está pensado para su uso con SQL Server.</span><span class="sxs-lookup"><span data-stu-id="32b9c-105">It's intended for use by SQL Server.</span></span><span data-ttu-id="32b9c-106"> Para otras bases de datos, utilice el mecanismo de hospedaje proporcionado por esa base de datos.</span><span class="sxs-lookup"><span data-stu-id="32b9c-106"> For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public virtual void Close ();
```

## <a name="remarks"></a><span data-ttu-id="32b9c-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="32b9c-107">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="32b9c-108">El `SqlStreamChars.Close` método es privado y no está pensado para usarse directamente en el código.</span><span class="sxs-lookup"><span data-stu-id="32b9c-108">The `SqlStreamChars.Close` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="32b9c-109">Microsoft no admite el uso de este campo en una aplicación de producción bajo ninguna circunstancia.</span><span class="sxs-lookup"><span data-stu-id="32b9c-109">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b9c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32b9c-110">Requirements</span></span>

<span data-ttu-id="32b9c-111">**Espacio de nombres:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="32b9c-111">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="32b9c-112">**Ensamblado:** System.Data (en System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="32b9c-112">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="32b9c-113">**Versiones de .NET framework:** Disponible desde la versión 2.0.</span><span class="sxs-lookup"><span data-stu-id="32b9c-113">**.NET Framework versions:** Available since 2.0.</span></span>