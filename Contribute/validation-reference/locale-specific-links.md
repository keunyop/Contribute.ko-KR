# <a name="locale-specific-links"></a><span data-ttu-id="272ba-101">로캘별 링크</span><span class="sxs-lookup"><span data-stu-id="272ba-101">Locale-specific links</span></span>

<span data-ttu-id="272ba-102">`en-us`와 같은 로캘 코드는 특정 Microsoft 사이트에 연결된 링크에 포함하지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="272ba-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="272ba-103">영어 콘텐츠에 있는 링크에 로캘 코드를 포함하면 로캘 코드가 지역화된 링크에도 포함되어 잘못된 지역화된 환경이 생성될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272ba-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="272ba-104">예를 들어 독일의 지역화된 콘텐츠에 있는 링크에 `en-us`가 포함되어 있으면 독일어 버전이 있어도 독일어 고객이 영어 문서에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="272ba-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="272ba-105">Microsoft 사이트에 연결된 링크에서 로캘 코드를 제거하세요.</span><span class="sxs-lookup"><span data-stu-id="272ba-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="272ba-106">다음은 한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="272ba-106">The following is an example.</span></span>

<span data-ttu-id="272ba-107">이전:</span><span class="sxs-lookup"><span data-stu-id="272ba-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="272ba-108">이후:</span><span class="sxs-lookup"><span data-stu-id="272ba-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="272ba-109">다음 사이트는 이 유효성 검사의 범위에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="272ba-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="272ba-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="272ba-110">azure.microsoft.com</span></span>
- <span data-ttu-id="272ba-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="272ba-111">docs.microsoft.com</span></span>
- <span data-ttu-id="272ba-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="272ba-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="272ba-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="272ba-113">technet.microsoft.com</span></span>