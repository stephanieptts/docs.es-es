---
title: "StrongNameKeyGenEx (Función)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: StrongNameKeyGenEx
api_location: mscoree.dll
api_type: DLLExport
f1_keywords: StrongNameKeyGenEx
helpviewer_keywords: StrongNameKeyGenEx function [.NET Framework strong naming]
ms.assetid: 36bd10b9-9857-45f3-8d3b-0da091d6169e
topic_type: apiref
caps.latest.revision: "17"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 87841c230c71650f822a6cb2f6cc3f3c17c2ef35
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="strongnamekeygenex-function"></a><span data-ttu-id="e4f68-102">StrongNameKeyGenEx (Función)</span><span class="sxs-lookup"><span data-stu-id="e4f68-102">StrongNameKeyGenEx Function</span></span>
<span data-ttu-id="e4f68-103">Genera un nuevo par de claves pública/privada con el tamaño de clave especificado, para su uso de nombre seguro.</span><span class="sxs-lookup"><span data-stu-id="e4f68-103">Generates a new public/private key pair with the specified key size, for strong name use.</span></span>  
  
 <span data-ttu-id="e4f68-104">Esta función está desusada.</span><span class="sxs-lookup"><span data-stu-id="e4f68-104">This function has been deprecated.</span></span> <span data-ttu-id="e4f68-105">Use la [ICLRStrongName:: StrongNameKeyGenEx](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygenex-method.md) método en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e4f68-105">Use the [ICLRStrongName::StrongNameKeyGenEx](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygenex-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4f68-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4f68-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameKeyGenEx (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  DWORD     dwFlags,  
    [in]  DWORD     dwKeySize,  
    [out] BYTE      **ppbKeyBlob,  
    [out] ULONG     *pcbKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e4f68-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4f68-107">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="e4f68-108">[in] El nombre de contenedor de claves solicitado.</span><span class="sxs-lookup"><span data-stu-id="e4f68-108">[in] The requested key container name.</span></span> <span data-ttu-id="e4f68-109">`wszKeyContainer`debe ser una cadena no vacía o null para generar un nombre temporal.</span><span class="sxs-lookup"><span data-stu-id="e4f68-109">`wszKeyContainer` must be a non-empty string, or null to generate a temporary name.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="e4f68-110">[in] Especifica si se debe abandonar la clave registrada.</span><span class="sxs-lookup"><span data-stu-id="e4f68-110">[in] Specifies whether to leave the key registered.</span></span> <span data-ttu-id="e4f68-111">Se admiten los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e4f68-111">The following values are supported:</span></span>  
  
-   <span data-ttu-id="e4f68-112">0 x 00000000: se usa cuando `wszKeyContainer` es null para generar un nombre de contenedor de claves temporal.</span><span class="sxs-lookup"><span data-stu-id="e4f68-112">0x00000000 - Used when `wszKeyContainer` is null to generate a temporary key container name.</span></span>  
  
-   <span data-ttu-id="e4f68-113">0 x 00000001 (`SN_LEAVE_KEY`)-especifica que la clave debería quedar registrada.</span><span class="sxs-lookup"><span data-stu-id="e4f68-113">0x00000001 (`SN_LEAVE_KEY`) - Specifies that the key should be left registered.</span></span>  
  
 `dwKeySize`  
 <span data-ttu-id="e4f68-114">[in] El tamaño solicitado de la clave en bits.</span><span class="sxs-lookup"><span data-stu-id="e4f68-114">[in] The requested size of the key, in bits.</span></span>  
  
 `ppbKeyBlob`  
 <span data-ttu-id="e4f68-115">[out] El par de claves pública y privada devuelto.</span><span class="sxs-lookup"><span data-stu-id="e4f68-115">[out] The returned public/private key pair.</span></span>  
  
 `pcbKeyBlob`  
 <span data-ttu-id="e4f68-116">[out] El tamaño, en bytes, de `ppbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="e4f68-116">[out] The size, in bytes, of `ppbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e4f68-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4f68-117">Return Value</span></span>  
 <span data-ttu-id="e4f68-118">`true`Cuando se finaliza correctamente; en caso contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="e4f68-118">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e4f68-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4f68-119">Remarks</span></span>  
 <span data-ttu-id="e4f68-120">Las versiones de .NET Framework 1.0 y 1.1 requieren un `dwKeySize` de 1024 bits para firmar un ensamblado con un nombre seguro; la versión 2.0 también admite claves de 2048 bits de.</span><span class="sxs-lookup"><span data-stu-id="e4f68-120">The .NET Framework versions 1.0 and 1.1 require a `dwKeySize` of 1024 bits to sign an assembly with a strong name; version 2.0 adds supports for 2048-bit keys.</span></span>  
  
 <span data-ttu-id="e4f68-121">Una vez recuperada la clave, debe llamar a la [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) función para liberar la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="e4f68-121">After the key is retrieved, you should call the [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) function to release the allocated memory.</span></span>  
  
 <span data-ttu-id="e4f68-122">Si el `StrongNameKeyGenEx` función no se completan correctamente, llame a la [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) función para recuperar el último error generado.</span><span class="sxs-lookup"><span data-stu-id="e4f68-122">If the `StrongNameKeyGenEx` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4f68-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4f68-123">Requirements</span></span>  
 <span data-ttu-id="e4f68-124">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e4f68-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4f68-125">**Encabezado:** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="e4f68-125">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="e4f68-126">**Biblioteca:** incluye como recurso en MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e4f68-126">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e4f68-127">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4f68-127">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4f68-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4f68-128">See Also</span></span>  
 [<span data-ttu-id="e4f68-129">StrongNameKeyGenEx (método)</span><span class="sxs-lookup"><span data-stu-id="e4f68-129">StrongNameKeyGenEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygenex-method.md)  
 [<span data-ttu-id="e4f68-130">StrongNameKeyGen (método)</span><span class="sxs-lookup"><span data-stu-id="e4f68-130">StrongNameKeyGen Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygen-method.md)  
 [<span data-ttu-id="e4f68-131">ICLRStrongName (interfaz)</span><span class="sxs-lookup"><span data-stu-id="e4f68-131">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)