---
title: IMetaDataEmit2 (Interfaz)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit2
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit2
helpviewer_keywords: IMetaDataEmit2 interface [.NET Framework metadata]
ms.assetid: 866dc96b-bbfc-4c0f-80c2-38ce93072106
topic_type: apiref
caps.latest.revision: "14"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 235134c66395f04a87ed4f3325f5cc4cd9fecfc8
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataemit2-interface"></a><span data-ttu-id="5f511-102">IMetaDataEmit2 (Interfaz)</span><span class="sxs-lookup"><span data-stu-id="5f511-102">IMetaDataEmit2 Interface</span></span>
<span data-ttu-id="5f511-103">Extiende la [IMetaDataEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interfaz principalmente para proporcionar la capacidad de trabajar con tipos genéricos.</span><span class="sxs-lookup"><span data-stu-id="5f511-103">Extends the [IMetaDataEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface primarily to provide the ability to work with generic types.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5f511-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f511-104">Methods</span></span>  
  
|<span data-ttu-id="5f511-105">Método</span><span class="sxs-lookup"><span data-stu-id="5f511-105">Method</span></span>|<span data-ttu-id="5f511-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f511-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5f511-107">DefineGenericParam (método)</span><span class="sxs-lookup"><span data-stu-id="5f511-107">DefineGenericParam Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definegenericparam-method.md)|<span data-ttu-id="5f511-108">Crea una definición para un parámetro de tipo genérico y obtiene un símbolo (token) para ese parámetro de tipo genérico.</span><span class="sxs-lookup"><span data-stu-id="5f511-108">Creates a definition for a generic type parameter, and gets a token to that generic type parameter.</span></span>|  
|[<span data-ttu-id="5f511-109">DefineMethodSpec (método)</span><span class="sxs-lookup"><span data-stu-id="5f511-109">DefineMethodSpec Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definemethodspec-method.md)|<span data-ttu-id="5f511-110">Crea una instancia de un método genérica y obtiene un símbolo (token) a la definición.</span><span class="sxs-lookup"><span data-stu-id="5f511-110">Creates a generic instance of a method, and gets a token to the definition.</span></span>|  
|[<span data-ttu-id="5f511-111">GetDeltaSaveSize (método)</span><span class="sxs-lookup"><span data-stu-id="5f511-111">GetDeltaSaveSize Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-getdeltasavesize-method.md)|<span data-ttu-id="5f511-112">Obtiene un valor que indica la diferencia de tamaño de los datos que es necesaria para expresar los cambios para la sesión actual de editar y continuar.</span><span class="sxs-lookup"><span data-stu-id="5f511-112">Gets a value indicating the difference in size of the data that is required to express the changes for the current edit-and-continue session.</span></span>|  
|[<span data-ttu-id="5f511-113">ResetENCLog (método)</span><span class="sxs-lookup"><span data-stu-id="5f511-113">ResetENCLog Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-resetenclog-method.md)|<span data-ttu-id="5f511-114">Restablece el registro Editar y continuar e inicia una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="5f511-114">Resets the edit-and-continue log and starts a new session.</span></span>|  
|[<span data-ttu-id="5f511-115">SaveDelta (método)</span><span class="sxs-lookup"><span data-stu-id="5f511-115">SaveDelta Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-savedelta-method.md)|<span data-ttu-id="5f511-116">Guarda los cambios de la sesión actual de editar y continuar en el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="5f511-116">Saves changes from the current edit-and-continue session to the specified file.</span></span>|  
|[<span data-ttu-id="5f511-117">SaveDeltaToMemory (método)</span><span class="sxs-lookup"><span data-stu-id="5f511-117">SaveDeltaToMemory Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-savedeltatomemory-method.md)|<span data-ttu-id="5f511-118">Guarda los cambios de la sesión actual de editar y continuar en la memoria.</span><span class="sxs-lookup"><span data-stu-id="5f511-118">Saves changes from the current edit-and-continue session to memory.</span></span>|  
|[<span data-ttu-id="5f511-119">SaveDeltaToStream (método)</span><span class="sxs-lookup"><span data-stu-id="5f511-119">SaveDeltaToStream Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-savedeltatostream-method.md)|<span data-ttu-id="5f511-120">Guarda los cambios de la sesión actual de editar y continuar en la secuencia especificada.</span><span class="sxs-lookup"><span data-stu-id="5f511-120">Saves changes from the current edit-and-continue session to the specified stream.</span></span>|  
|[<span data-ttu-id="5f511-121">SetGenericParamProps (método)</span><span class="sxs-lookup"><span data-stu-id="5f511-121">SetGenericParamProps Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-setgenericparamprops-method.md)|<span data-ttu-id="5f511-122">Establece los valores de propiedad para la definición de parámetro genérico al que hace referencia el token especificado.</span><span class="sxs-lookup"><span data-stu-id="5f511-122">Sets property values for the generic parameter definition referenced by the specified token.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5f511-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f511-123">Requirements</span></span>  
 <span data-ttu-id="5f511-124">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5f511-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f511-125">**Encabezado:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="5f511-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5f511-126">**Biblioteca:** usada como recurso en MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5f511-126">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5f511-127">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f511-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f511-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f511-128">See Also</span></span>  
 [<span data-ttu-id="5f511-129">Interfaces de metadatos</span><span class="sxs-lookup"><span data-stu-id="5f511-129">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)  
 [<span data-ttu-id="5f511-130">IMetaDataEmit (interfaz)</span><span class="sxs-lookup"><span data-stu-id="5f511-130">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)