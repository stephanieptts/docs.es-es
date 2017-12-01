---
title: "ICLRStrongName::StrongNameTokenFromAssembly (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRStrongName.StrongNameTokenFromAssembly
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRStrongName::StrongNameTokenFromAssembly
helpviewer_keywords:
- ICLRStrongName::StrongNameTokenFromAssembly method [.NET Framework hosting]
- StrongNameTokenFromAssembly method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: fc725afb-b66b-4015-aa44-1c0d1304197f
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 0b236fe3b041277401c2983cf229981253c01328
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="iclrstrongnamestrongnametokenfromassembly-method"></a><span data-ttu-id="da834-102">ICLRStrongName::StrongNameTokenFromAssembly (Método)</span><span class="sxs-lookup"><span data-stu-id="da834-102">ICLRStrongName::StrongNameTokenFromAssembly Method</span></span>
<span data-ttu-id="da834-103">Crea un token de nombre seguro del archivo de ensamblado especificado.</span><span class="sxs-lookup"><span data-stu-id="da834-103">Creates a strong name token from the specified assembly file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da834-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da834-104">Syntax</span></span>  
  
```  
HRESULT StrongNameTokenFromAssembly (  
    [in]  LPCWSTR   wszFilePath,  
    [out] BYTE      **ppbStrongNameToken,  
    [out] ULONG     *pcbStrongNameToken  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="da834-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da834-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="da834-106">[in] La ruta de acceso al archivo ejecutable portable (PE) para el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="da834-106">[in] The path to the portable executable (PE) file for the assembly.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="da834-107">[out] El token de nombre seguro devuelto.</span><span class="sxs-lookup"><span data-stu-id="da834-107">[out] The returned strong name token.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="da834-108">[out] El tamaño, en bytes, del token de nombre seguro.</span><span class="sxs-lookup"><span data-stu-id="da834-108">[out] The size, in bytes, of the strong name token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="da834-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da834-109">Return Value</span></span>  
 <span data-ttu-id="da834-110">`S_OK`Si el método se completó correctamente; en caso contrario, un valor HRESULT que indica un error (vea [valores HRESULT comunes](http://go.microsoft.com/fwlink/?LinkId=213878) para obtener una lista).</span><span class="sxs-lookup"><span data-stu-id="da834-110">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="da834-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da834-111">Remarks</span></span>  
 <span data-ttu-id="da834-112">Un token de nombre seguro es la forma abreviada de una clave pública.</span><span class="sxs-lookup"><span data-stu-id="da834-112">A strong name token is the shortened form of a public key.</span></span> <span data-ttu-id="da834-113">El token es un hash de 64 bits que se crea a partir de la clave pública utilizada para firmar el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="da834-113">The token is a 64-bit hash that is created from the public key used to sign the assembly.</span></span> <span data-ttu-id="da834-114">El token forma parte del nombre seguro del ensamblado y se puede leer desde los metadatos del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="da834-114">The token is a part of the strong name for the assembly, and can be read from the assembly metadata.</span></span>  
  
 <span data-ttu-id="da834-115">Una vez creado el token, debe llamar a la [ICLRStrongName:: StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) método para liberar la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="da834-115">After the token is created, you should call the [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) method to release the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da834-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da834-116">Requirements</span></span>  
 <span data-ttu-id="da834-117">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="da834-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="da834-118">**Encabezado:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="da834-118">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="da834-119">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="da834-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="da834-120">**Versiones de .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="da834-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da834-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="da834-121">See Also</span></span>  
 [<span data-ttu-id="da834-122">StrongNameTokenFromAssemblyEx (método)</span><span class="sxs-lookup"><span data-stu-id="da834-122">StrongNameTokenFromAssemblyEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassemblyex-method.md)  
 [<span data-ttu-id="da834-123">ICLRStrongName (interfaz)</span><span class="sxs-lookup"><span data-stu-id="da834-123">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)