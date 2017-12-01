---
title: "ICorDebugCode2::GetCodeChunks (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugCode2.GetCodeChunks
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugCode2::GetCodeChunks
helpviewer_keywords:
- GetCodeChunks method [.NET Framework debugging]
- ICorDebugCode2::GetCodeChunks method [.NET Framework debugging]
ms.assetid: 210a2f02-2678-4555-bc4a-78a0408764c8
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 950fd5c19e8827a63dcf075c42d3e0c18ff91261
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugcode2getcodechunks-method"></a><span data-ttu-id="3c3b8-102">ICorDebugCode2::GetCodeChunks (Método)</span><span class="sxs-lookup"><span data-stu-id="3c3b8-102">ICorDebugCode2::GetCodeChunks Method</span></span>
<span data-ttu-id="3c3b8-103">Obtiene los fragmentos de código de los que está compuesto este objeto de código.</span><span class="sxs-lookup"><span data-stu-id="3c3b8-103">Gets the chunks of code that this code object is composed of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c3b8-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c3b8-104">Syntax</span></span>  
  
```  
HRESULT GetCodeChunks (  
    [in]  ULONG32     cbufSize,  
    [out] ULONG32     *pcnumChunks,  
    [out, size_is(cbufSize), length_is(*pcnumChunks)]   
        CodeChunkInfo chunks[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3c3b8-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c3b8-105">Parameters</span></span>  
 `cbufSize`  
 <span data-ttu-id="3c3b8-106">[in] Tamaño de la `chunks` matriz.</span><span class="sxs-lookup"><span data-stu-id="3c3b8-106">[in] Size of the `chunks` array.</span></span>  
  
 `pcnumChunks`  
 <span data-ttu-id="3c3b8-107">[out] El número de fragmentos que se devuelven en el `chunks` matriz.</span><span class="sxs-lookup"><span data-stu-id="3c3b8-107">[out] The number of chunks returned in the `chunks` array.</span></span>  
  
 `chunks`  
 <span data-ttu-id="3c3b8-108">[out] Una matriz de estructuras de "CodeChunkInfo", cada uno de los cuales representa un único fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="3c3b8-108">[out] An array of "CodeChunkInfo" structures, each of which represents a single chunk of code.</span></span> <span data-ttu-id="3c3b8-109">Si el valor de `cbufSize` es 0, este parámetro puede ser null.</span><span class="sxs-lookup"><span data-stu-id="3c3b8-109">If the value of `cbufSize` is 0, this parameter can be null.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3c3b8-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c3b8-110">Remarks</span></span>  
 <span data-ttu-id="3c3b8-111">Los fragmentos de código nunca se superpondrán y siguen el orden en el que habría concatenados [ICorDebugCode:: GetCode](../../../../docs/framework/unmanaged-api/debugging/icordebugcode-getcode-method.md).</span><span class="sxs-lookup"><span data-stu-id="3c3b8-111">The code chunks will never overlap, and they will follow the order in which they would have been concatenated by [ICorDebugCode::GetCode](../../../../docs/framework/unmanaged-api/debugging/icordebugcode-getcode-method.md).</span></span> <span data-ttu-id="3c3b8-112">Un objeto de código de lenguaje intermedio (MSIL) de Microsoft en la versión 2.0 de .NET Framework se forman parte de un único fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="3c3b8-112">A Microsoft intermediate language (MSIL) code object in the .NET Framework version 2.0 will comprise a single code chunk.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c3b8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c3b8-113">Requirements</span></span>  
 <span data-ttu-id="3c3b8-114">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3c3b8-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c3b8-115">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3c3b8-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3c3b8-116">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c3b8-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c3b8-117">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c3b8-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c3b8-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c3b8-118">See Also</span></span>  
 