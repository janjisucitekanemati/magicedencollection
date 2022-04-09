# MagicEden.io Public API

[https://api.magiceden.dev/](https://api.magiceden.dev/)

# MagicEden.io RPC

[JSON RPC Specification](https://www.jsonrpc.org/specification)

## Get Listed NFTs By Query

**URL** : `https://api-mainnet.magiceden.dev/rpc/getListedNFTsByQuery`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|nowait|true/false|
|q|{"$match":{"collectionSymbol":"cops_game"},"$sort":{"createdAt":-1},"$skip":0,"$limit":20}|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.dev/rpc/getListedNFTsByQuery?q=%7B%22%24match%22%3A%7B%22collectionSymbol%22%3A%22cops_game%22%7D%2C%22%24sort%22%3A%7B%22createdAt%22%3A-1%7D%2C%22%24skip%22%3A0%2C%22%24limit%22%3A20%7D", {
    "credentials": "include",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8",
        "Accept-Language": "en-GB,en;q=0.5",
        "Upgrade-Insecure-Requests": "1",
        "Sec-Fetch-Dest": "document",
        "Sec-Fetch-Mode": "navigate",
        "Sec-Fetch-Site": "cross-site",
        "Sec-Fetch-User": "?1",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "symbol": "astrals",
    "categories": [
      "pfps",
      "games"
    ],
    "createdAt": "2022-03-10T00:15:57.032Z",
    "derivativeDetails": {
      "originName": "",
      "originLink": ""
    },
    "description": "10,000 unique 3d avatars, 200 traits, 16 races, 3500 PX renders with masterfully crafted lore. Astrals is a community-driven project with aspirations of galactic proportions featuring the incredible character design art of Damien Guimoneau. Each Astral is your gateway to our Galaxy DAO and to stake to mine $GLXY - our governance token. Our goal as a community will be to bridge the gap between Solana and the Universe.",
    "discord": "https://www.discord.gg/astralsnft",
    "enabledAttributesFilters": true,
    "image": "https://creator-hub-prod.s3.us-east-2.amazonaws.com/astrals_pfp_1649437133503.png",
    "isDerivative": false,
    "name": "ASTRALS",
    "totalItems": 10000,
    "twitter": "https://www.twitter.com/Astrals_NFT",
    "website": "https://astralsnft.io/",
    "updatedAt": "2022-04-09T04:23:35.286Z",
    "watchlistCount": 1181,
    "isDraft": false,
    "nftImageType": "",
    "onChainCollectionAddress": "",
    "rarity": {
      "showHowrare": true,
      "showMoonrank": true
    },
    "hasAllItems": false
  }
]
```

---

## Get Activities By Query

**URL** : `https://api-mainnet.magiceden.dev/rpc/getActivitiesByQuery`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|nowait|true/false|
|q|{"$match":{"$or":[{"seller_address":"4cnM34f2HNAeKPy71pRvPA3gFDMJZKCDH1aYJEKVk19e"},{"buyer_address":"4cnM34f2HNAeKPy71pRvPA3gFDMJZKCDH1aYJEKVk19e"}]},"$sort":{"blockTime":-1},"$skip":0}|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.dev/rpc/getActivitiesByQuery?q=%7B%22%24match%22%3A%7B%22%24or%22%3A%5B%7B%22seller_address%22%3A%224cnM34f2HNAeKPy71pRvPA3gFDMJZKCDH1aYJEKVk19e%22%7D%2C%7B%22buyer_address%22%3A%224cnM34f2HNAeKPy71pRvPA3gFDMJZKCDH1aYJEKVk19e%22%7D%5D%7D%2C%22%24sort%22%3A%7B%22blockTime%22%3A-1%7D%2C%22%24skip%22%3A0%7D", {
    "credentials": "include",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8",
        "Accept-Language": "en-GB,en;q=0.5",
        "Upgrade-Insecure-Requests": "1",
        "Sec-Fetch-Dest": "document",
        "Sec-Fetch-Mode": "navigate",
        "Sec-Fetch-Site": "cross-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "symbol": "astrals",
    "categories": [
      "pfps",
      "games"
    ],
    "createdAt": "2022-03-10T00:15:57.032Z",
    "derivativeDetails": {
      "originName": "",
      "originLink": ""
    },
    "description": "10,000 unique 3d avatars, 200 traits, 16 races, 3500 PX renders with masterfully crafted lore. Astrals is a community-driven project with aspirations of galactic proportions featuring the incredible character design art of Damien Guimoneau. Each Astral is your gateway to our Galaxy DAO and to stake to mine $GLXY - our governance token. Our goal as a community will be to bridge the gap between Solana and the Universe.",
    "discord": "https://www.discord.gg/astralsnft",
    "enabledAttributesFilters": true,
    "image": "https://creator-hub-prod.s3.us-east-2.amazonaws.com/astrals_pfp_1649437133503.png",
    "isDerivative": false,
    "name": "ASTRALS",
    "totalItems": 10000,
    "twitter": "https://www.twitter.com/Astrals_NFT",
    "website": "https://astralsnft.io/",
    "updatedAt": "2022-04-09T04:23:35.286Z",
    "watchlistCount": 1181,
    "isDraft": false,
    "nftImageType": "",
    "onChainCollectionAddress": "",
    "rarity": {
      "showHowrare": true,
      "showMoonrank": true
    },
    "hasAllItems": false
  }
]
```

---

## Get Collections With Symbols

**URL** : `https://api-mainnet.magiceden.dev/rpc/getCollectionsWithSymbols`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|nowait|true/false|
|edge_cache|true/false|
|symbols|[":symbolName"]|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.dev/rpc/getCollectionsWithSymbols?symbols=%5B%22solana_monkey_business%22%5D&edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "symbol": "astrals",
    "categories": [
      "pfps",
      "games"
    ],
    "createdAt": "2022-03-10T00:15:57.032Z",
    "derivativeDetails": {
      "originName": "",
      "originLink": ""
    },
    "description": "10,000 unique 3d avatars, 200 traits, 16 races, 3500 PX renders with masterfully crafted lore. Astrals is a community-driven project with aspirations of galactic proportions featuring the incredible character design art of Damien Guimoneau. Each Astral is your gateway to our Galaxy DAO and to stake to mine $GLXY - our governance token. Our goal as a community will be to bridge the gap between Solana and the Universe.",
    "discord": "https://www.discord.gg/astralsnft",
    "enabledAttributesFilters": true,
    "image": "https://creator-hub-prod.s3.us-east-2.amazonaws.com/astrals_pfp_1649437133503.png",
    "isDerivative": false,
    "name": "ASTRALS",
    "totalItems": 10000,
    "twitter": "https://www.twitter.com/Astrals_NFT",
    "website": "https://astralsnft.io/",
    "updatedAt": "2022-04-09T04:23:35.286Z",
    "watchlistCount": 1181,
    "isDraft": false,
    "nftImageType": "",
    "onChainCollectionAddress": "",
    "rarity": {
      "showHowrare": true,
      "showMoonrank": true
    },
    "hasAllItems": false
  }
]
```

---

to be continue
https://api-mainnet.magiceden.dev/rpc/getBiddingsByQuery?q={%22$match%22:{%22initializerDepositTokenMintAccount%22:{%22$in%22:[mintTokens]}},%22$sort%22:{%22createdAt%22:-1}}

https://api-mainnet.magiceden.dev/rpc/getNFTByMintAddress

https://api-mainnet.magiceden.dev/rpc/getNFTsByOwner/:wallet

https://api-mainnet.magiceden.dev/rpc/getNFTStatsByMintAddress/:mintaddress

https://api-mainnet.magiceden.dev/rpc/getGlobalActivitiesByQuery{"$match":{"collection_symbol":"stoned_ape_crew"},"$sort":{"blockTime":-1,"createdAt":-1},"$skip":0}

https://api-mainnet.magiceden.dev/rpc/getCollectionEscrowStats/space_runners


# MagicEden.io Undocumented API

## Featured Carousels

**URL** : `https://api-mainnet.magiceden.io/featured_carousels`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/featured_carousels?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "_id": "624b8d9fad7bc10011a9363e",
    "description": "We are Solana's #1 marketplace! Check out some of our curated collections below 👇",
    "image": "https://dl.airtable.com/.attachments/af7f9cc33de0f9abc14153c2a0c6ffcf/56460aa1/ETHfrens1.gif",
    "title": "Welcome to Magic Eden!",
    "index": 0,
    "publishedAt": null,
    "removedAt": null,
    "url": ""
  }
]
```

---

## Featured Collections Carousels

**URL** : `https://api-mainnet.magiceden.io/featured_collections_carousels`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/featured_collections_carousels?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "_id": "6210cfdf82216400117a2f6c",
    "title": "Launchpad Drops",
    "index": 0,
    "collections": [],
    "type": "upcoming-launches",
    "publishedAt": null,
    "removedAt": null
  }
]
```

---

## Popular Collections

**URL** : `https://api-mainnet.magiceden.io/popular_collections`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|
|more|true/false|
|timeRang|1d/7d/30d|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/popular_collections?timeRange=1d&edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
{
  "collections": [
    {
      "_id": "61e20147fd5137001097cedb",
      "symbol": "degods",
      "candyMachineIds": [
        "8RMqBV79p8sb51nMaKMWR94XKjUvD2kuUSAkpEJTmxyx"
      ],
      "name": "DeGods",
      "image": "https://i.imgur.com/fO3tI1t.png",
      "categories": [
        "pfps",
        "art"
      ],
      "description": "A collection of degenerates, punks, and misfits. Gods of the metaverse & masters of our own universe. DeGods can be converted to DeadGods with DUST.",
      "createdAt": "2022-01-14T23:03:33.857Z",
      "enabledAttributesFilters": true,
      "isDraft": false,
      "website": "https://degods.com/",
      "twitter": "https://twitter.com/degodsnft",
      "discord": "https://discord.com/invite/dedao",
      "derivativeDetails": {
        "originLink": "",
        "originName": ""
      },
      "isDerivative": false,
      "nftImageType": "",
      "rarity": {
        "showHowrare": false,
        "showMoonrank": false
      },
      "updatedAt": "2022-04-09T04:32:02.174Z",
      "watchlistCount": 1294,
      "onChainCollectionAddress": ""
    }
  ]
}
```

---

## Drops

**URL** : `https://api-mainnet.magiceden.io/drops`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|
|top|10/?|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/drops?edge_cache=true&top=10", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "name": "Decimus Dynamics",
    "symbol": "decimusdynamics",
    "description": "It is the year 3081. The Earth is now a desolate landscape uninhabitable for the human race. A group of aliens, the Zeons invaded the Earth and decimated the population of Earth with chemicals and poisonous gasses. These chemicals have an adverse effect on the Earth's raccoon population and enhance their mental capacities to levels beyond former human intelligence. These now mentally enhanced raccoons have headed underground and started building a new civilization. They create 4000 robots they can pilot, first to help with digging and moving things too heavy for their small bodies, but after years underground there is unrest between different factions of the raccoon civilization.",
    "assets": {
      "profileImage": "https://creator-hub-prod.s3.us-east-2.amazonaws.com/decimusdynamics_pfp_1648575083383.png"
    },
    "derivative": null,
    "links": {
      "twitter": "https://twitter.com/DecimusDynamic",
      "discord": "https://discord.gg/Decimus"
    },
    "launchDate": "2022-04-09T17:00:00.000Z",
    "isMeLaunchPad": false,
    "upvote": 428
  }
]
```

---

## Auctions

**URL** : `https://api-mainnet.magiceden.io/auctions`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/auctions?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "_id": "61f973d054b68f00116723c9",
    "type": "english",
    "slug": "zodiac_snake",
    "configId": "JDZ1Zokxa2K3WDkNE82FKHqHmJpq23s2Y3Z4DCD5p9ZT",
    "name": "Zodiac Collection: Snake",
    "description": "Thousands of years ago, the Zodiac Calendar was created as a way to measure time. The first twelve animals to cross a fast flowing river would have a year named after them.  Inspired by eastern calligraphy, Snake is one of twelve unique pieces from my Zodiac Collection, bringing ancient legend to the forefront of blockchain technology.   Celebrated by a quarter of the world, the Lunar New Year is a time of giving, family, prosperity, food and among many other things, spending time together.  Wishing you a prosperous Lunar New Year.  xoxo  Ms Zenith",
    "creatorName": "Ms Zenith",
    "websiteLink": "https://mszenith.my.canva.site/",
    "discordLink": "",
    "twitterLink": "https://twitter.com/MsZenithArt",
    "imageWidth": 1000,
    "imageHeight": 1000,
    "published": true,
    "featured": false,
    "collection": "MSZ",
    "config": {
      "bump": 254,
      "authority": "HYPJr6AErcnQ4kJj8UVojReNJnY3jH6KpbQFfBL2HDxM",
      "minBid": 1000000000,
      "minBidIncrement": 500000000,
      "startDate": "2022-02-02T17:00:00.000Z",
      "endDate": "2022-02-04T02:10:00.000Z",
      "tokenAccount": "4wWoQ7JEUfZubXQY55g5SsrvuobZDTVjxXZ1yRksyNnS",
      "tokenMint": "EuS4tqpKQu3detrLrZA8ZDznPjnQ2ZVdrRAYJihtpkFF",
      "highestBid": "FmtCEcYYVVVhHqTXLbAefcE7UKFDDuzpRLoN5i7EuuKc",
      "highestBidAmount": 2500000000,
      "highestBidder": "6JzXsCwJKiGH9o29HCveDyLD7TyioY3qAmTQthSdEvfP",
      "acceptingBids": true,
      "auctionClosed": true,
      "timeExtension": 600,
      "timeExtensionThreshold": 600
    },
    "updatedAt": "2022-02-19T20:48:00.178Z"
  }
]
```

---

## Highest Sold NFTs

**URL** : `https://api-mainnet.magiceden.io/highest_sold_nfts`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|
|more|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/highest_sold_nfts?more=true&edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
{
  "result": [
    {
      "nft": {
        "id": "FwyM7d7nXwo4qTwWZffDdvx4VSgQpsrEA6fuKWHJ9Vpw",
        "price": 0,
        "owner": "4ZGWPgjMNGHMrUJqyLFzEk92XDJwUFvyaAWbSm17ueHC",
        "collectionName": "portals",
        "collectionTitle": "Portals",
        "img": "https://arweave.net/Kpi85acYI9i9HZVnnhRuO3Vi_1XDpshHx80eGA3mhD4?ext=jpg",
        "title": "Portals | Onyx #256",
        "content": "This expansive space strikes the perfect balance of splendor and functionality.",
        "animationURL": "https://arweave.net/SuRJK0fVU2Mg1L0qIJggeNQsWhHz7HUOboS9-gGhPAg?ext=mp4",
        "propertyCategory": "video",
        "creators": [
          {
            "address": "5grvMeoBqv5ZdHq9JMy5RrxLPNAt1nzc9cpqYWFUwizz",
            "verified": 1,
            "share": 0
          },
          {
            "address": "EmdsWm9dJ1d6BgQzHDcMJkDvB5SVvpfrAtpiGMVW1gxx",
            "verified": 1,
            "share": 0
          },
          {
            "address": "GdtkQajEADGbfSUEBS5zctYrhemXYQkqnrMiGY7n7vAw",
            "verified": 0,
            "share": 100
          }
        ],
        "sellerFeeBasisPoints": 500,
        "mintAddress": "3KGGHD48w6JtePqfLhtiH2N2yBxm9yTGJpWXRN2EYk5o",
        "attributes": [
          {
            "trait_type": "Unit Type",
            "value": "Onyx"
          },
          {
            "trait_type": "Unit Number",
            "value": 256
          }
        ],
        "properties": {
          "files": [
            {
              "uri": "https://arweave.net/Kpi85acYI9i9HZVnnhRuO3Vi_1XDpshHx80eGA3mhD4?ext=jpg",
              "type": "image/jpeg"
            },
            {
              "uri": "https://arweave.net/SuRJK0fVU2Mg1L0qIJggeNQsWhHz7HUOboS9-gGhPAg?ext=mp4",
              "type": "video/mp4"
            }
          ],
          "category": "video",
          "creators": [
            {
              "address": "EmdsWm9dJ1d6BgQzHDcMJkDvB5SVvpfrAtpiGMVW1gxx",
              "share": 0
            },
            {
              "address": "GdtkQajEADGbfSUEBS5zctYrhemXYQkqnrMiGY7n7vAw",
              "share": 100
            }
          ]
        },
        "supply": 1,
        "updateAuthority": "EmdsWm9dJ1d6BgQzHDcMJkDvB5SVvpfrAtpiGMVW1gxx",
        "primarySaleHappened": 1,
        "onChainCollection": {},
        "tokenDelegateValid": false
      },
      "totalAmount": 333000000000
    }
  ]
}
```

---

## New Collections

**URL** : `https://api-mainnet.magiceden.io/new_collections`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|
|more|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/new_collections?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
{
  "collections": [
    {
      "symbol": "zuixmetadream",
      "categories": [
        "art",
        "virtual_worlds"
      ],
      "createdAt": "2022-04-09T04:46:20.894Z",
      "derivativeDetails": {
        "originName": "",
        "originLink": ""
      },
      "description": "1/1 Uniques NFT's ✔ is an attempt to recreate the fantastical dreamworlds we all experience every night through the lens of AI. By combining the power of language interpretation and visual perception using a highly customized VQGAN+CLIP pipeline, the pieces in this collection each evoke their own unique dreamworld that should be experienced rather than understood",
      "discord": "https://www.discord.gg/PM7t6q7N",
      "enabledAttributesFilters": true,
      "image": "https://creator-hub-prod.s3.us-east-2.amazonaws.com/zuixmetadream_pfp_1649473565172.jpeg",
      "isDerivative": false,
      "name": "Zuix METADREAM ART",
      "totalItems": 13,
      "twitter": "https://www.twitter.com/Zuix_Arts"
    }
  ]
}
```

---

## Volumes

**URL** : `https://api-mainnet.magiceden.io/volumes`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/volumes?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
{
  "total": 9583951.24066862,
  "last24Hrs": 65142.248224952,
  "last7Days": 511836.551518149,
  "last30Days": 2157121.574039251
}
```

---

## Volumes

**URL** : `https://api-mainnet.magiceden.io/globalWarning`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/globalWarning", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
{
  "_id": "62487d10bea360023ded4888",
  "active": false,
  "dismissable": false,
  "tooltipText": "",
  "warningText": "",
  "tpsThreshold": 1800,
  "severity": "Warning"
}
```

---

## All Collections With Escrow Data

**URL** : `https://api-mainnet.magiceden.io/all_collections_with_escrow_data`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/all_collections_with_escrow_data?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
{
  "collections": [
    {
      "symbol": "komodo_lizardz",
      "categories": [
        "pfps",
        "art"
      ],
      "createdAt": "2022-04-09T04:31:28.426Z",
      "derivativeDetails": {
        "originName": "",
        "originLink": ""
      },
      "description": "455⠀Komodo⠀Lizardz⠀in⠀Solana.⠀Stake2Earn⠀$ZARD,⠀Breed⠀and⠀Much⠀More.",
      "discord": "https://www.discord.gg/fxQ9X9Yeng",
      "enabledAttributesFilters": true,
      "image": "https://creator-hub-prod.s3.us-east-2.amazonaws.com/komodo_lizardz_pfp_1649431771365.jpeg",
      "isDerivative": false,
      "name": "Komodo Lizardz",
      "totalItems": 455,
      "twitter": "https://www.twitter.com/KomodoLizardz",
      "volumeAll": 0
    }
  ]
}
```

---

## All Organizations

**URL** : `https://api-mainnet.magiceden.io/all_organizations`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/all_organizations?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "name": "Moshiheads",
    "symbol": "moshiheads",
    "description": "3,000 Moshiheads sworn to protect the Solana space from evil sludge monsters.",
    "assets": {
      "bannerImage": "https://bafkreibz4ccegtopq7l5okdle5an2iwu75ysza363hwkeh4xb7ea5se6qm.ipfs.nftstorage.link/"
    },
    "links": {
      "twitter": "https://twitter.com/Moshiheads",
      "discord": "https://discord.gg/moshiheads",
      "website": "http://moshiheads.com/"
    }
  }
]
```

---

## Launchpad Collections

**URL** : `https://api-mainnet.magiceden.io/launchpad_collections`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/launchpad_collections?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "_id": "6157eb8106fcd7a36e3664ec",
    "symbol": "zoolana",
    "name": "Zoolana",
    "description": "Zoolana is a play-and-earn social strategy game being built for mobile. Players will collect resources, control units, and rally with their tribe to take on opponents in the Zoolana valley.\nThe Teaser Edition is Zoolana's historic first mint and illustrated by industry leading concept artists. Holders will have a chance to win our Alpha Edition NFT dropping in early November which is the VIP pass for Zoolana. People who hold Alpha Edition can expect airdrops of an in-game character + monthly equipment NFTs + other freebies and perks!",
    "published": true,
    "mint": {
      "candyMachineId": "3iNYkwM1q3Fgz4NJHy2i5A12Tn5nXZD2tHrjpiPWFA7z",
      "config": "JDwQWA9rngVxmUqLmVSF564iHZKYgjQtzrUHNaAyFSaQ",
      "treasury": "6QNWBWhxBfEMkwBUTeTsGyxohBicA3k6EGWr6X8KmzUL"
    },
    "image": "https://i.imgur.com/L2PGzor.gif",
    "launchDate": "2021-10-15T19:00:00.000Z",
    "price": 0.00001,
    "size": 2550,
    "updatedAt": "2022-01-30T06:00:47.039Z",
    "createdAt": "2022-01-26T06:13:53.357Z",
    "__v": 0,
    "featured": false
  }
]
```

---

## Launchpad Collections

**URL** : `https://api-mainnet.magiceden.io/launchpad_collections`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/launchpad_collections?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "_id": "6157eb8106fcd7a36e3664ec",
    "symbol": "zoolana",
    "name": "Zoolana",
    "description": "Zoolana is a play-and-earn social strategy game being built for mobile. Players will collect resources, control units, and rally with their tribe to take on opponents in the Zoolana valley.\nThe Teaser Edition is Zoolana's historic first mint and illustrated by industry leading concept artists. Holders will have a chance to win our Alpha Edition NFT dropping in early November which is the VIP pass for Zoolana. People who hold Alpha Edition can expect airdrops of an in-game character + monthly equipment NFTs + other freebies and perks!",
    "published": true,
    "mint": {
      "candyMachineId": "3iNYkwM1q3Fgz4NJHy2i5A12Tn5nXZD2tHrjpiPWFA7z",
      "config": "JDwQWA9rngVxmUqLmVSF564iHZKYgjQtzrUHNaAyFSaQ",
      "treasury": "6QNWBWhxBfEMkwBUTeTsGyxohBicA3k6EGWr6X8KmzUL"
    },
    "image": "https://i.imgur.com/L2PGzor.gif",
    "launchDate": "2021-10-15T19:00:00.000Z",
    "price": 0.00001,
    "size": 2550,
    "updatedAt": "2022-01-30T06:00:47.039Z",
    "createdAt": "2022-01-26T06:13:53.357Z",
    "__v": 0,
    "featured": false
  }
]
```

---

## New Games

**URL** : `https://api-mainnet.magiceden.io/new_games`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/new_games?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "symbol": "hockey_heroes",
    "candyMachineIds": [],
    "name": "Hockey Heroes",
    "image": "https://dl.airtable.com/.attachmentThumbnails/f6aefbc5e2334b7e388027960a9ef5a5/a0816e97",
    "categories": [
      "sports"
    ],
    "description": "The greatest hockey NFT collection on #Solana. 3333 packs hide 111 all-star players claimable as rare physical collectibles.",
    "createdAt": "2022-02-15T01:35:51.837Z",
    "enabledAttributesFilters": true,
    "isDraft": false,
    "website": "https://t.co/pcsS7KvFI2",
    "twitter": "https://twitter.com/hockeyheroes_io",
    "discord": "https://t.co/qnwwhIomeS",
    "derivativeDetails": {
      "originLink": "",
      "originName": ""
    },
    "isDerivative": false,
    "nftImageType": "",
    "flagMessage": "",
    "isFlagged": false,
    "updatedAt": "2022-04-08T16:08:38.394Z",
    "watchlistCount": 10
  }
]
```

---

## Popular Games

**URL** : `https://api-mainnet.magiceden.io/popular_games`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/popular_games?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
[
  {
    "symbol": "yaku_corp",
    "candyMachineIds": [],
    "name": "Yaku Engineering ONI-S01",
    "image": "https://bafybeidykoipw77pm7ivk52vmbduvxzx6tj4tyrgjc6fskcon5usb45n2m.ipfs.nftstorage.link/",
    "categories": [
      "games",
      "virtual_worlds"
    ],
    "description": "YAKU Engineering ONI-S01 is the first playable customizable motorcycle in the Yakuverse - Race your way in search of $YAKU on these Seisui technology powered motorcycles.",
    "createdAt": "2022-02-15T19:09:33.442Z",
    "enabledAttributesFilters": true,
    "isDraft": false,
    "website": "http://yakushima.io/",
    "twitter": "https://twitter.com/yakucorp?s=21",
    "discord": "https://discord.gg/MH6u9cEcZz",
    "derivativeDetails": {
      "originLink": "",
      "originName": ""
    },
    "isDerivative": false,
    "nftImageType": "",
    "rarity": {
      "showHowrare": false,
      "showMoonrank": false
    },
    "updatedAt": "2022-04-09T05:21:34.154Z",
    "watchlistCount": 516,
    "onChainCollectionAddress": ""
  }
]
```

---

## Get Aggregated Collection Metrics

**URL** : `https://api-mainnet.magiceden.io/getAggregatedCollectionMetrics`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|
|timeframe|1d/7d/30d|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/rpc/getAggregatedCollectionMetrics?timeframe=1d&edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
{
  "results": [
    {
      "_id": "61c8187186e5dc0f9ac46c69",
      "symbol": "floofers",
      "name": "Floofers",
      "date": "2022-04-09",
      "totalItems": 0,
      "image": "https://dl.airtable.com/.attachmentThumbnails/1bb43aa8410073b5a44c2514eebc7be8/a2229815",
      "txVolume": {
        "valueAT": 16.79299,
        "value1d": 0,
        "prev1d": 0,
        "delta1d": 0,
        "value1dME": 0
      },
      "avgPrice": {
        "valueAT": 0.25443924242424243,
        "value1d": 0.08,
        "prev1d": 0.08,
        "delta1d": 1
      },
      "floorPrice": {
        "value1d": 0.09,
        "prev1d": 0.09,
        "delta1d": 1
      },
      "txVolumeME": {
        "valueAT": 16.61299,
        "value1d": 0,
        "prev1d": 0,
        "delta1d": 0
      }
    }
  ]
}
```

---

## Get Aggregated Marketplace Metrics

**URL** : `https://api-mainnet.magiceden.io/getAggregatedMarketplaceMetrics`

**Method** : `GET`

**Public** : NO

**Auth required** : NO

### Query Parameters

| Name | Value |
|:---|:---|
|edge_cache|true/false|
|timeframe|1d/7d/30d|

### Request examples**

```js
await fetch("https://api-mainnet.magiceden.io/rpc/getAggregatedMarketplaceMetrics?edge_cache=true", {
    "credentials": "omit",
    "headers": {
        "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:99.0) Gecko/20100101 Firefox/99.0",
        "Accept": "application/json, text/plain, */*",
        "Accept-Language": "en-GB,en;q=0.5",
        "Sec-Fetch-Dest": "empty",
        "Sec-Fetch-Mode": "cors",
        "Sec-Fetch-Site": "same-site",
        "Pragma": "no-cache",
        "Cache-Control": "no-cache"
    },
    "referrer": "https://magiceden.io/",
    "method": "GET",
    "mode": "cors"
});
```

### Success Response

**Code** : `200 OK`

**Content examples**

```json
{
  "results": [
    {
      "name": "Magic Eden",
      "txVolume": {
        "value1d": 63867.841089802,
        "value7d": 511078.290558699,
        "value30d": 2155436.94161858
      },
      "txCount": {
        "value1d": 21850,
        "value7d": 192032,
        "value30d": 819760
      },
      "activeWallets": {
        "value1d": 20262,
        "value7d": 79667,
        "value30d": 182092
      }
    }
  ]
}
```

---
