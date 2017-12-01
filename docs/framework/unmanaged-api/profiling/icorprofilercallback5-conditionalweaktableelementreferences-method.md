---
title: "ICorProfilerCallback5::ConditionalWeakTableElementReferences (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback5.ConditionalWeakTableReferences
api_location: Mscorwks.dll
api_type: COM
f1_keywords: CondiitonalWeakTableElementReferences
helpviewer_keywords:
- ConditionalWeakTableElementReferences method, ICorProfilerCallback5 interface [.NET Framework profiling]
- ICorProfilerCallback5::ConditionalWeakTableElementReferences method [.NET Framework profiling]
ms.assetid: 532c7a02-a9de-4cea-bb2b-7f470da594de
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 386cbffea565e6864a77132b96756c073e33fc6d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilercallback5conditionalweaktableelementreferences-method"></a><span data-ttu-id="0e326-102">ICorProfilerCallback5::ConditionalWeakTableElementReferences (Método)</span><span class="sxs-lookup"><span data-stu-id="0e326-102">ICorProfilerCallback5::ConditionalWeakTableElementReferences Method</span></span>
<span data-ttu-id="0e326-103">Identifica el cierre transitivo de los objetos a los que esas raíces hacen referencia mediante referencias directas de campo de miembro y mediante dependencias `ConditionalWeakTable`.</span><span class="sxs-lookup"><span data-stu-id="0e326-103">Identifies the transitive closure of objects referenced by those roots through both direct member field references and through `ConditionalWeakTable` dependencies.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e326-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e326-104">Syntax</span></span>  
  
```  
HRESULT ConditionalWeakTableElementReferences(     [in]                     ULONG    cRootRefs,     [in, size_is(cRootRefs)] ObjectID keyRefIds[],     [in, size_is(cRootRefs)] ObjectID valueRefIds[],     [in, size_is(cRootRefs)] GCHandleID rootIds[]);};  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0e326-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e326-105">Parameters</span></span>  
 `cRootRefs`  
 <span data-ttu-id="0e326-106">[in] Número de elementos en las matrices `keyRefIds`, `valueRefIds` y `rootIds`.</span><span class="sxs-lookup"><span data-stu-id="0e326-106">[in] The number of elements in the `keyRefIds`, `valueRefIds`, and `rootIds` arrays.</span></span>  
  
 `keyRefIds`  
 <span data-ttu-id="0e326-107">[in] Matriz de identificadores de objeto, cada uno de los cuales contiene el `ObjectID` del elemento principal en el par de controladores de dependencia.</span><span class="sxs-lookup"><span data-stu-id="0e326-107">[in] An array of object IDs, each of which contains the `ObjectID` for the primary element in the dependent handle pair.</span></span>  
  
 `valueRefIds`  
 <span data-ttu-id="0e326-108">[in] Matriz de identificadores de objeto, cada uno de los cuales contiene el `ObjectID` del elemento secundario en el par de controladores de dependencia.</span><span class="sxs-lookup"><span data-stu-id="0e326-108">[in] An array of object IDs, each of which contains the `ObjectID` for the secondary element in the dependent handle pair.</span></span> <span data-ttu-id="0e326-109">(`keyRefIds[i]` mantiene `valueRefIds[i]` activo.)</span><span class="sxs-lookup"><span data-stu-id="0e326-109">(`keyRefIds[i]` keeps `valueRefIds[i]` alive.)</span></span>  
  
 `rootIds`  
 <span data-ttu-id="0e326-110">[in] Matriz de valores `GCHandleID` que apuntan a un entero que contiene información adicional sobre la raíz de recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="0e326-110">[in] An array of `GCHandleID` values that point to an integer that contains additional information about the garbage collection root.</span></span>  
  
 <span data-ttu-id="0e326-111">Ninguno de los valores `ObjectID` devueltos por el método `ConditionalWeakTableElementReferences` son válidos durante la devolución de llamada en sí, porque el recolector de elementos no utilizados puede estar en proceso de mover objetos de ubicaciones anteriores a nuevas.</span><span class="sxs-lookup"><span data-stu-id="0e326-111">None of the `ObjectID` values returned by the `ConditionalWeakTableElementReferences` method are valid during the callback itself, because the garbage collector may be in the process of moving objects from old to new locations.</span></span> <span data-ttu-id="0e326-112">Por lo tanto, los generadores de perfiles no deben intentar inspeccionar objetos durante una llamada a `ConditionalWeakTableElementReferences`.</span><span class="sxs-lookup"><span data-stu-id="0e326-112">Therefore, profilers should not attempt to inspect objects during a `ConditionalWeakTableElementReferences` call.</span></span> <span data-ttu-id="0e326-113">En `GarbageCollectionFinished`, todos los objetos se han movido a sus nuevas ubicaciones y puede que la inspección se haya realizado.</span><span class="sxs-lookup"><span data-stu-id="0e326-113">At `GarbageCollectionFinished`, all objects have been moved to their new locations, and inspection may be done.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0e326-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e326-114">Example</span></span>  
 <span data-ttu-id="0e326-115">En el ejemplo de código siguiente se muestra cómo implementar [ICorProfilerCallback5](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-interface.md) y usar este método.</span><span class="sxs-lookup"><span data-stu-id="0e326-115">The following code example demonstrates how to implement [ICorProfilerCallback5](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-interface.md) and use this method.</span></span>  
  
```  
HRESULT Callback5Impl::ConditionalWeakTableElementReferences(  
    ULONG      cRootRefs,  
    ObjectID   keyRefIds[],  
    ObjectID   valueRefIds[],  
    GCHandleID rootIds[])  
{  
    printf("Callback5Impl::ConditionalWeakTableElementReferences called\n");  
    for (unsigned int i = 0; i < cRootRefs; ++i)  
    {  
        // Save dependency to XML for later retrieval  
        PersistDependencyToXml(rootIds[i], keyRefIds[i], valueRefIds[i]);  
        // or store dependency to an internal map  
        m_cwt_deps->add_dep(rootIds[i], keyRefIds[i], valueRefIds[i]);  
        // or add arc to object graph  
        m_obj_graph->add_arc(keyRefIds[i], valueRefIds[i], rootIds[i]);  
    }  
    return S_OK;  
}  
```  
  
## <a name="remarks"></a><span data-ttu-id="0e326-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e326-116">Remarks</span></span>  
 <span data-ttu-id="0e326-117">Un generador de perfiles para la [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)] o versiones posteriores implementa la [ICorProfilerCallback5](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-interface.md) interfaz y registra las dependencias especificadas por el `ConditionalWeakTableElementReferences` método.</span><span class="sxs-lookup"><span data-stu-id="0e326-117">A profiler for the [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)] or later versions implements the [ICorProfilerCallback5](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-interface.md) interface and records the dependencies specified by the `ConditionalWeakTableElementReferences` method.</span></span> <span data-ttu-id="0e326-118">`ICorProfilerCallback5`proporciona el conjunto completo de las dependencias entre objetos activos representados por `ConditionalWeakTable` entradas.</span><span class="sxs-lookup"><span data-stu-id="0e326-118">`ICorProfilerCallback5` provides the complete set of dependencies among live objects represented by `ConditionalWeakTable` entries.</span></span> <span data-ttu-id="0e326-119">Estas dependencias y el miembro de campo referencias especificadas por el [ICorProfilerCallback:: ObjectReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectreferences-method.md) método habilitar un generador de perfiles administrado generar el gráfico de objetos completo de objetos activos.</span><span class="sxs-lookup"><span data-stu-id="0e326-119">These dependencies and the member field references specified by the [ICorProfilerCallback::ObjectReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectreferences-method.md) method enable a managed profiler to generate the full object graph of live objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e326-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e326-120">Requirements</span></span>  
 <span data-ttu-id="0e326-121">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0e326-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0e326-122">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0e326-122">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0e326-123">**Versiones de .NET framework:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0e326-123">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e326-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e326-124">See Also</span></span>  
 [<span data-ttu-id="0e326-125">ICorProfilerCallback5 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="0e326-125">ICorProfilerCallback5 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-interface.md)