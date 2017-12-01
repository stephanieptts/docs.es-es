---
title: ICorDebugRegisterSet2 (Interfaz)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugRegisterSet2
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugRegisterSet2
helpviewer_keywords: ICorDebugRegisterSet2 interface [.NET Framework debugging]
ms.assetid: d7fbccbf-3b6b-4db8-a96d-768e1cb6b1a6
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 26967f50ded62f935a705c25eed58314b77bedd8
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugregisterset2-interface"></a><span data-ttu-id="b9e16-102">ICorDebugRegisterSet2 (Interfaz)</span><span class="sxs-lookup"><span data-stu-id="b9e16-102">ICorDebugRegisterSet2 Interface</span></span>
<span data-ttu-id="b9e16-103">Amplía las capacidades de la [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) interfaz para plataformas de hardware que tienen más de 64 registros.</span><span class="sxs-lookup"><span data-stu-id="b9e16-103">Extends the capabilities of the [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) interface for hardware platforms that have more than 64 registers.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b9e16-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9e16-104">Methods</span></span>  
  
|<span data-ttu-id="b9e16-105">Método</span><span class="sxs-lookup"><span data-stu-id="b9e16-105">Method</span></span>|<span data-ttu-id="b9e16-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9e16-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b9e16-107">GetRegisters (método)</span><span class="sxs-lookup"><span data-stu-id="b9e16-107">GetRegisters Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-getregisters-method.md)|<span data-ttu-id="b9e16-108">Obtiene el valor de cada registro (en el equipo que está ejecutando el código) especificado por la máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="b9e16-108">Gets the value of each register (on the computer that is currently executing code) that is specified by the bit mask.</span></span>|  
|[<span data-ttu-id="b9e16-109">GetRegistersAvailable (método)</span><span class="sxs-lookup"><span data-stu-id="b9e16-109">GetRegistersAvailable Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-getregistersavailable-method.md)|<span data-ttu-id="b9e16-110">Obtiene una matriz de bytes que proporciona un mapa de bits de los registros disponibles.</span><span class="sxs-lookup"><span data-stu-id="b9e16-110">Gets an array of bytes that provides a bitmap of the available registers.</span></span>|  
|[<span data-ttu-id="b9e16-111">SetRegisters (método)</span><span class="sxs-lookup"><span data-stu-id="b9e16-111">SetRegisters Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-setregisters-method.md)|<span data-ttu-id="b9e16-112">No se implementa en la versión 2.0 de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b9e16-112">Not implemented in the .NET Framework version 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b9e16-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b9e16-113">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b9e16-114">Esta interfaz no admite que se la llame de forma remota, ya sea entre procesos o entre equipos.</span><span class="sxs-lookup"><span data-stu-id="b9e16-114">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9e16-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9e16-115">Requirements</span></span>  
 <span data-ttu-id="b9e16-116">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b9e16-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9e16-117">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b9e16-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b9e16-118">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b9e16-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b9e16-119">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b9e16-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9e16-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9e16-120">See Also</span></span>  
 [<span data-ttu-id="b9e16-121">Interfaces de depuración</span><span class="sxs-lookup"><span data-stu-id="b9e16-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="b9e16-122">ICorDebugRegisterSet (interfaz)</span><span class="sxs-lookup"><span data-stu-id="b9e16-122">ICorDebugRegisterSet Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)