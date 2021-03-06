---



copyright:

  years: 2017, 2018
lastupdated: "2018-11-19"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# 變更方案
{: #changing}

您可以變更 {{site.data.keyword.Bluemix}} 服務方案（如果已啟用該服務的方案變更）。您可能想要變更方案，例如，升級或降低方案。您可以從服務實例儀表板變更方案。
{: shortdesc}

您在尋找關於升級帳戶類型的詳細資料嗎？如需相關資訊，請參閱[如何升級或變更我的帳戶類型？](/docs/account/account_faq.html#changeacct)。
{: tip}

您只能針對特定服務變更服務方案。如果已啟用服務的方案變更，則服務實例儀表板會在導覽中顯示**方案**選項。如果您變更方案，則每一個服務都會有要遵循的不同後續步驟集。

1. 按一下服務實例儀表板中的**方案**。您一般可以升級方案，或降低方案。
2. 在變更方案之後，您必須完成額外步驟。步驟會視方案變更類型及服務而不同。例如，如果您降低方案，則可能需要重新編譯打包應用程式。或者，如果您升級方案，則可能需要重新編譯打包應用程式，然後採取其他動作。

若要重新編譯打包應用程式，請移至資源清單，尋找服務所連結的應用程式。按一下「功能表」圖示 ![「功能表」圖示](../icons/icon_hamburger.svg)** > 資源清單**。在應用程式功能表中，選取**重新啟動應用程式**。

其他後續步驟動作是與服務相依。如需特定動作，請參閱下表。

|服務|	資訊|
|--------|-------------|
|Presence Insights 	|如果您有 Lite 方案，並超出免費額度，則會顯示 403 訊息，或記載此訊息以指出您不再獲得授權，並且停用服務實例。同時，還會以 403 回應來拒絕 POST REST API 呼叫。<br/><br/>如果因超出免費額度而停用您的服務，您可以從「精簡」方案升級為「付費」方案。您的服務會在 2 小時內重新予以啟用。<br/><br/>如果您具有「付費」方案，則只要事件及總儲存空間的用量維持在「精簡」方案額度內，就可以將方案降低為「精簡」方案。<br/><br/>當您升級或降低方案時，不需要重新編譯打包或重新啟動應用程式。|
{:caption="表 1. 變更方案的後續步驟" caption-side="top"}


## 透過指令行介面變更方案
{: #changing_command_line}

您可以選擇透過指令行介面，輸入下列指令來變更服務方案：

```
cf update-service <service_name> [-p <new_plan>]
```
