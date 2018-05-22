### <a name="deflatestream-uses-native-apis-for-decompression"></a><span data-ttu-id="d32df-101">DeflateStream usa las API nativas para la descompresión</span><span class="sxs-lookup"><span data-stu-id="d32df-101">DeflateStream uses native APIs for decompression</span></span>

|   |   |
|---|---|
|<span data-ttu-id="d32df-102">Detalles</span><span class="sxs-lookup"><span data-stu-id="d32df-102">Details</span></span>|<span data-ttu-id="d32df-103">A partir de .NET Framework 4.7.2, la implementación de la descompresión en la clase <code>T:System.IO.Compression.DeflateStream</code> ha cambiado para usar las API nativas de Windows de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d32df-103">Starting with the .NET Framework 4.7.2, the implementation of decompression in the <code>T:System.IO.Compression.DeflateStream</code> class has changed to use native Windows APIs by default.</span></span> <span data-ttu-id="d32df-104">Normalmente, esto da como resultado una mejora considerable del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d32df-104">Typically, this results in a substantial performance improvement.</span></span> <span data-ttu-id="d32df-105">En todas las aplicaciones de .NET que tienen como destino la versión 4.7.2 de .NET Framework o una versión posterior se usa la implementación nativa. Es posible que este cambio provoque algunas diferencias de comportamiento, como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="d32df-105">All .NET applications targeting the .NET Framework version 4.7.2 or higher use the native implementation.This change might result in some differences in behavior, which include:</span></span><ul><li><span data-ttu-id="d32df-106">Los mensajes de excepción pueden ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="d32df-106">Exception messages may be different.</span></span> <span data-ttu-id="d32df-107">Pero el tipo de excepción que se inicia sigue siendo el mismo.</span><span class="sxs-lookup"><span data-stu-id="d32df-107">However, the type of exception thrown remains the same.</span></span></li><li><span data-ttu-id="d32df-108">Algunas situaciones especiales, por ejemplo no tener memoria suficiente para completar una operación, se pueden administrar de otra manera.</span><span class="sxs-lookup"><span data-stu-id="d32df-108">Some special situations, such as not having enough memory to complete an operation, may be handled differently.</span></span></li><li><span data-ttu-id="d32df-109">Hay diferencias conocidas para el análisis del encabezado de gzip (Nota: Solo se ve afectado <code>GZipStream</code> establecido para la descompresión):</span><span class="sxs-lookup"><span data-stu-id="d32df-109">There are known differences for parsing gzip header (note: only <code>GZipStream</code> set for decompression is affected):</span></span></li><li><span data-ttu-id="d32df-110">Se pueden iniciar excepciones al analizar encabezados no válidos en momentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="d32df-110">Exceptions when parsing invalid headers may be thrown at different times.</span></span></li><li><span data-ttu-id="d32df-111">La implementación nativa exige que los valores para algunas marcas reservadas dentro del encabezado de gzip (es decir, [FLG](http://www.zlib.org/rfc-gzip.html#header-trailer)) se establezcan según la especificación, lo que puede provocar que se inicie una excepción donde anteriormente se ignoraban los valores no válidos.</span><span class="sxs-lookup"><span data-stu-id="d32df-111">The native implementation enforces that values for some reserved flags inside the gzip header (i.e. [FLG](http://www.zlib.org/rfc-gzip.html#header-trailer)) are set according to the specification, which may cause it to throw an exception where previously invalid values were ignored.</span></span></li></ul>|
|<span data-ttu-id="d32df-112">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="d32df-112">Suggestion</span></span>|<span data-ttu-id="d32df-113">Si la descompresión con las API nativas ha afectado negativamente el comportamiento de la aplicación, puede descartar esta característica si agrega el modificador <code>Switch.System.IO.Compression.DoNotUseNativeZipLibraryForDecompression</code> a la sección <code>runtime</code> del archivo app.config y lo establece en <code>true</code>:</span><span class="sxs-lookup"><span data-stu-id="d32df-113">If decompression with native APIs has adversely affected the behavior of your app, you can opt out of this feature by adding the <code>Switch.System.IO.Compression.DoNotUseNativeZipLibraryForDecompression</code> switch to the <code>runtime</code> section of your app.config file and setting it to <code>true</code>:</span></span><pre><code class="lang-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot; ?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.IO.Compression.DoNotUseNativeZipLibraryForDecompression=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="d32df-114">Ámbito</span><span class="sxs-lookup"><span data-stu-id="d32df-114">Scope</span></span>|<span data-ttu-id="d32df-115">Secundaria</span><span class="sxs-lookup"><span data-stu-id="d32df-115">Minor</span></span>|
|<span data-ttu-id="d32df-116">Versión</span><span class="sxs-lookup"><span data-stu-id="d32df-116">Version</span></span>|<span data-ttu-id="d32df-117">4.7.2</span><span class="sxs-lookup"><span data-stu-id="d32df-117">4.7.2</span></span>|
|<span data-ttu-id="d32df-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="d32df-118">Type</span></span>|<span data-ttu-id="d32df-119">Redestinación</span><span class="sxs-lookup"><span data-stu-id="d32df-119">Retargeting</span></span>|
|<span data-ttu-id="d32df-120">API afectadas</span><span class="sxs-lookup"><span data-stu-id="d32df-120">Affected APIs</span></span>|<ul><li><xref:System.IO.Compression.DeflateStream?displayProperty=nameWithType></li><li><xref:System.IO.Compression.GZipStream?displayProperty=nameWithType></li></ul>|
