---
-api-id: M:Windows.Web.AtomPub.AtomPubClient.RetrieveFeedAsync(Windows.Foundation.Uri)
-api-type: winrt method
---

<!-- Method syntax
public Windows.Foundation.IAsyncOperationWithProgress<Windows.Web.Syndication.SyndicationFeed, Windows.Web.Syndication.RetrievalProgress> RetrieveFeedAsync(Windows.Foundation.Uri uri)
-->

# Windows.Web.AtomPub.AtomPubClient.RetrieveFeedAsync

## -description
Starts an asynchronous operation to download the syndication feed from the given URI. This method instantiates a [SyndicationFeed](../windows.web.syndication/syndicationfeed.md) object from the feed string, which can be in one of the formats specified in [SyndicationFormat](../windows.web.syndication/syndicationformat.md).

## -parameters
### -param uri
The URI from which the feed is downloaded.

## -returns
Contains the results of the operation.

## -remarks

## -examples
The following code demonstrates how a feed is retrieved at a specific service address using [AtomPubClient](atompubclient.md). For additional examples of how AtomPub can be used to manage feed content, download the [AtomPub sample](https://go.microsoft.com/fwlink/p/?linkid=245061).

```javascript

    function retieveFeed() {
        try {
            // Refresh client in case server url or credential have changed.
            createClient();

            // Note that this feed is public by default and will not require authentication.
            // We will only get back a limited use feed, without information about editing.
            var resourceUri = new Windows.Foundation.Uri(document.getElementById("serviceAddressField").value.trim() + defaultFeedUri);

            outputField.innerHTML = "Fetching resource: " + resourceUri.absoluteUri + "/br";
            client.retrieveFeedAsync(resourceUri).done(function (feed) {
                currentFeed = feed;
                currentItemIndex = 0;

                outputField.innerHTML += "Complete</br>";
                displayCurrentItem();
            }, onError);
        }
        catch (ex) {
            outputField.innerHTML += "Exception:" + ex + "</br>";
        }
    }
```



## -see-also
[Quickstart: Managing Feed Entries](https://msdn.microsoft.com/library/239d42bc-5812-4ead-a91c-b3696fc3ef75), [AtomPub sample](https://go.microsoft.com/fwlink/p/?linkid=245061)
