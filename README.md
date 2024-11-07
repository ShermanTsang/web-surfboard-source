# web-surfboard-source
`Source` is a collection of websites (most of them are providing a way to search).

Use WebSurfboard extension to subscribe the source will help user to access the websites search service easily.

You can create and maintain your websites source for users to subscribe in WebSurfboard extension.

## File format

User can subscribe your source by the url of the source file.

Example: [official source](https://ws.shermant.com/websites.json)

The type definition of `Source` is as follows:

```typescript
  interface Source {
    url: string
    maintainer?: string
    email?: string
    version: string
    description?: string
    name: string
    projectUrl?: string
    websites: Item[]
    latestUpdatedAt?: number
  }
```

The corresponding JSON data format is as follows:

```json
{
    "url": "https://example.com",
    "maintainer": "example",
    "email": "example@example.com",
    "version": "1.0.0",
    "description": "example description",
    "name": "example",
    "projectUrl": "https://example.com",
}
```

## Website item

The type definition of `Item` is as follows:

```typescript
  interface Item {
    category: string
    name: string
    favIcon: string
    domain: string
    sortOrder: number
    searchParams: string
  }
```

Corresponding JSON data format is as follows:

```json
{
    "category": "example",
    "name": "example",
    "favIcon": "example",
    "domain": "example",
    "sortOrder": 0,
    "searchParams": "example"
}
```

For instance, the `searchParams` is refer to the search query string.

```json
// https://example.com/search?q=example
{
    "searchParams": "q=example"
}
```

## Official source

This repository is the official source of WebSurfboard extension.

If you want to add your source to the official source, please open an issue or submit a pull request.

Edit the excel file `source.xlsx` and submit a pull request.


