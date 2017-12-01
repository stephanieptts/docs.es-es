---
title: "Clone (función) (referencia de API no administrada)"
description: "La función de clonación devuelve un nuevo objeto que es un clon completo del actual."
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: Clone
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: Clone
helpviewer_keywords: Clone function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: df6a089f66ddd6f8f9a2d5677dd8dd6917fcb719
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/15/2017
---
# <a name="clone-function"></a><span data-ttu-id="20d66-103">Clone (función)</span><span class="sxs-lookup"><span data-stu-id="20d66-103">Clone function</span></span>
<span data-ttu-id="20d66-104">Devuelve un nuevo objeto que es un clon completo del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="20d66-104">Returns a new object that is a complete clone of the current object.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="20d66-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20d66-105">Syntax</span></span>  
  
```  
HRESULT Clone (
   [in] int                  vFunc, 
   [in] IWbemClassObject*    ptr, 
   [out] IWbemClassObject**  ppCopy
); 
```  

## <a name="parameters"></a><span data-ttu-id="20d66-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20d66-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="20d66-107">[in] Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="20d66-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="20d66-108">[in] Un puntero a un [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) instancia.</span><span class="sxs-lookup"><span data-stu-id="20d66-108">[in] A pointer to an [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) instance.</span></span>

`ppCopy`  
<span data-ttu-id="20d66-109">[out] Un nuevo objeto que es una completa única de `ptr`.</span><span class="sxs-lookup"><span data-stu-id="20d66-109">[out] A new object that is a complete lone of `ptr`.</span></span> <span data-ttu-id="20d66-110">Este argumento no puede ser `null` si recibe la copia del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="20d66-110">This argument cannot be `null` if it receives the copy of the current object.</span></span>

## <a name="return-value"></a><span data-ttu-id="20d66-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20d66-111">Return value</span></span>

<span data-ttu-id="20d66-112">Los siguientes valores devueltos por esta función se definen en el *WbemCli.h* archivo de encabezado, o bien puede definirlas como constantes en el código:</span><span class="sxs-lookup"><span data-stu-id="20d66-112">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="20d66-113">Constante</span><span class="sxs-lookup"><span data-stu-id="20d66-113">Constant</span></span>  |<span data-ttu-id="20d66-114">Valor</span><span class="sxs-lookup"><span data-stu-id="20d66-114">Value</span></span>  |<span data-ttu-id="20d66-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="20d66-115">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_FAILED` | <span data-ttu-id="20d66-116">0 x 80041001</span><span class="sxs-lookup"><span data-stu-id="20d66-116">0x80041001</span></span> | <span data-ttu-id="20d66-117">Ha habido un error general.</span><span class="sxs-lookup"><span data-stu-id="20d66-117">There has been a general failure.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="20d66-118">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="20d66-118">0x80041008</span></span> | <span data-ttu-id="20d66-119">`null`se ha especificado como un parámetro, y no es válido en este uso.</span><span class="sxs-lookup"><span data-stu-id="20d66-119">`null` was specified as a parameter, and it is not legal in this usage.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="20d66-120">0 x 80041006</span><span class="sxs-lookup"><span data-stu-id="20d66-120">0x80041006</span></span> | <span data-ttu-id="20d66-121">No hay suficiente memoria disponible para clonar el objeto.</span><span class="sxs-lookup"><span data-stu-id="20d66-121">Not enough memory is available to clone the object.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="20d66-122">0</span><span class="sxs-lookup"><span data-stu-id="20d66-122">0</span></span> | <span data-ttu-id="20d66-123">La llamada de función tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="20d66-123">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="20d66-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20d66-124">Remarks</span></span>

<span data-ttu-id="20d66-125">Esta función contiene una llamada a la [IWbemClassObject::Clone](https://msdn.microsoft.com/library/aa391436(v=vs.85).aspx) método.</span><span class="sxs-lookup"><span data-stu-id="20d66-125">This function wraps a call to the [IWbemClassObject::Clone](https://msdn.microsoft.com/library/aa391436(v=vs.85).aspx) method.</span></span>

<span data-ttu-id="20d66-126">El objeto clonado es un objeto COM que tiene un recuento de referencias de 1.</span><span class="sxs-lookup"><span data-stu-id="20d66-126">The cloned object is a COM object that has a reference count of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="20d66-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20d66-127">Requirements</span></span>  
 <span data-ttu-id="20d66-128">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="20d66-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20d66-129">**Encabezado:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="20d66-129">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="20d66-130">**Versiones de .NET framework:**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="20d66-130">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20d66-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="20d66-131">See also</span></span>  
[<span data-ttu-id="20d66-132">WMI y contadores de rendimiento (referencia de API no administrada)</span><span class="sxs-lookup"><span data-stu-id="20d66-132">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)