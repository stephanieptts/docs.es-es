---
title: '&lt;quitar&gt; (elemento) para &lt;configSections&gt;'
ms.date: 05/01/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: article
f1_keywords: http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections/remove
helpviewer_keywords:
- remove Element
- <remove> Element
ms.assetid: ae4d82e0-e8fe-468c-81ab-46d63c4d66a8
author: guardrex
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: e6dfd1ac56070f55f30bd4bd093e1185486da295
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="remove-element-for-configsections"></a><span data-ttu-id="b02f5-102">\<Quitar > (elemento) para \<configSections ></span><span class="sxs-lookup"><span data-stu-id="b02f5-102">\<remove> element for \<configSections></span></span>

<span data-ttu-id="b02f5-103">Quita una sección predefinido o un grupo de sección.</span><span class="sxs-lookup"><span data-stu-id="b02f5-103">Removes a predefined section or section group.</span></span>

<span data-ttu-id="b02f5-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="b02f5-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="b02f5-105">&nbsp;&nbsp;[**\<configSections >**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="b02f5-105">&nbsp;&nbsp;[**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) </span></span>  
<span data-ttu-id="b02f5-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<Quitar >**</span><span class="sxs-lookup"><span data-stu-id="b02f5-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**</span></span>

## <a name="syntax"></a><span data-ttu-id="b02f5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b02f5-107">Syntax</span></span>

```xml
<remove name="section name or section group name" />
```

## <a name="attribute"></a><span data-ttu-id="b02f5-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="b02f5-108">Attribute</span></span>

|           | <span data-ttu-id="b02f5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b02f5-109">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="b02f5-110">**name**</span><span class="sxs-lookup"><span data-stu-id="b02f5-110">**name**</span></span>  | <span data-ttu-id="b02f5-111">Atributo necesario.</span><span class="sxs-lookup"><span data-stu-id="b02f5-111">Required attribute.</span></span><br><br><span data-ttu-id="b02f5-112">Especifica el nombre de la sección o el grupo de sección para quitar.</span><span class="sxs-lookup"><span data-stu-id="b02f5-112">Specifies the name of the section or section group to remove.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="b02f5-113">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="b02f5-113">Parent element</span></span>

|     | <span data-ttu-id="b02f5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b02f5-114">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="b02f5-115">**\<configSections >** elemento</span><span class="sxs-lookup"><span data-stu-id="b02f5-115">**\<configSections>** Element</span></span>](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) | <span data-ttu-id="b02f5-116">Contiene las declaraciones de espacio de nombres y la sección de configuración.</span><span class="sxs-lookup"><span data-stu-id="b02f5-116">Contains configuration section and namespace declarations.</span></span> |

# <a name="child-elements"></a><span data-ttu-id="b02f5-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b02f5-117">Child elements</span></span>

<span data-ttu-id="b02f5-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b02f5-118">None</span></span>

## <a name="remarks"></a><span data-ttu-id="b02f5-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b02f5-119">Remarks</span></span>

<span data-ttu-id="b02f5-120">Puede usar el  **\<quitar >** elemento que se va a quitar secciones y grupos de la aplicación que se han definido en un nivel superior en la jerarquía de archivos de configuración.</span><span class="sxs-lookup"><span data-stu-id="b02f5-120">You can use the **\<remove>** element to remove sections and section groups from your application that were defined at a higher level in the configuration file hierarchy.</span></span>

## <a name="example"></a><span data-ttu-id="b02f5-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b02f5-121">Example</span></span>

<span data-ttu-id="b02f5-122">En el ejemplo siguiente se muestra cómo utilizar el  **\<quitar >** elemento en un archivo de configuración de aplicación para quitar una sección definida anteriormente en el archivo de configuración del equipo.</span><span class="sxs-lookup"><span data-stu-id="b02f5-122">The following example shows how to use the **\<remove>** element in an application configuration file to remove a section previously defined in the machine configuration file.</span></span>

<span data-ttu-id="b02f5-123">El siguiente código de archivo de configuración del equipo declara la sección  **\<sampleSection >**:</span><span class="sxs-lookup"><span data-stu-id="b02f5-123">The following machine configuration file code declares the section **\<sampleSection>**:</span></span>

```xml
<!-- Machine.config file -->
<configuration>
  <configSections>
    <section name="sampleSection"
             type="System.Configuration.SingleTagSectionHandler" />
  </configSections>
  <sampleSection setting1="Value1" 
                 setting2="value two" 
                 setting3="third value" />
</configuration>
```

<span data-ttu-id="b02f5-124">El siguiente código de archivo de configuración de la aplicación quita el  **\<sampleSection >** sección.</span><span class="sxs-lookup"><span data-stu-id="b02f5-124">The following application configuration file code removes the **\<sampleSection>** section.</span></span> <span data-ttu-id="b02f5-125">Después de la eliminación, la aplicación no puede recuperar la configuración de  **\<sampleSection >**.</span><span class="sxs-lookup"><span data-stu-id="b02f5-125">After removal, the application cannot retrieve the settings in **\<sampleSection>**.</span></span>

```xml
<!-- Application configuration file -->
<configuration>
  <configSections>
    <remove name="sampleSection"/>
  </configSections>
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="b02f5-126">Archivo de configuración</span><span class="sxs-lookup"><span data-stu-id="b02f5-126">Configuration file</span></span>

<span data-ttu-id="b02f5-127">Este elemento se puede usar en el archivo de configuración de aplicación, archivo de configuración de máquina (*Machine.config*), y *Web.config* archivos que no están en el nivel de directorio de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b02f5-127">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="b02f5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b02f5-128">See also</span></span>

[<span data-ttu-id="b02f5-129">Esquema de archivos de configuración de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="b02f5-129">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)