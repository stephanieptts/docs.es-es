---
title: Herramientas adicionales de .NET Core
description: "Información general sobre las herramientas adicionales compatibles con las funcionalidades de .NET Core y que las amplían."
author: mlacouture
manager: wpickett
ms.author: johalex
ms.date: 01/19/2018
ms.topic: article
ms.prod: .net-core
ms.custom: mvc
ms.openlocfilehash: eac67285500e62501f3bb552deaf5b07db609d4e
ms.sourcegitcommit: 8bde7a3432f30fc771079744955c75c58c4eb393
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/20/2018
---
# <a name="net-core-additional-tools"></a>Herramientas adicionales de .NET Core
En esta sección se recopila una lista de herramientas compatibles con las funcionalidades de .NET Core y que las amplían, además de las herramientas de la [interfaz de la línea de comandos (CLI) de .NET Core](..\tools\index.md).

### <a name="wcf-web-service-reference-toolwcf-web-service-reference-guidemd"></a>[Herramienta WCF Web Service Reference](wcf-web-service-reference-guide.md)
WCF Web Services Reference es un proveedor de servicios conectados de Visual Studio que se estrenó en la [versión 15.5 de Visual Studio 2017](https://www.visualstudio.com/news/releasenotes/vs2017-relnotes#WCFTools). Esta herramienta recupera metadatos de un servicio web en la solución actual, en una ubicación de red o desde un archivo WSDL, y genera un archivo de origen compatible con .NET Core. El archivo contiene el código de proxy de cliente e Windows Communication Foundation (WCF) y podrá usarlo para acceder al servicio web.

### <a name="xml-serializer-generatorxmlserializergenerator-instructionsmd"></a>[Generador de serializador XML](xmlserializergenerator-instructions.md)
Tal y como sucede con el [generador serializador de XML (sgen.exe)](../../standard/serialization/xml-serializer-generator-tool-sgen-exe.md) para .NET Framework, el [paquete NuGet Microsoft.XmlSerializer.Generator](https://www.nuget.org/packages/Microsoft.XmlSerializer.Generator) es la solución para las bibliotecas .NET Core y .NET Standard. Crea un ensamblado de serialización de XML para los tipos contenidos en un ensamblado para mejorar el rendimiento de inicio de la serialización XML al serializar o deserializar objetos de esos tipos con <xref:System.Xml.Serialization.XmlSerializer>.