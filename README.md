# @komikhq/komikhq-typescript@1.2.0

A TypeScript SDK client for the nitro.komikhq.dpdns.org API.

## Usage

First, install the SDK from npm.

```bash
npm install @komikhq/komikhq-typescript --save
```

Next, try it out.


```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminCreateChapterOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // AdminCreateChapterRequest
    adminCreateChapterRequest: ...,
  } satisfies AdminCreateChapterOperationRequest;

  try {
    const data = await api.adminCreateChapter(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```


## Documentation

### API Endpoints

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Class | Method | HTTP request | Description
| ----- | ------ | ------------ | -------------
*AdministrationApi* | [**adminCreateChapter**](docs/AdministrationApi.md#admincreatechapteroperation) | **POST** /admin/chapters | Create comic chapter
*AdministrationApi* | [**adminCreateChapterPages**](docs/AdministrationApi.md#admincreatechapterpagesoperation) | **POST** /admin/chapters/{id}/pages | Set chapter pages
*AdministrationApi* | [**adminCreateComic**](docs/AdministrationApi.md#admincreatecomicoperation) | **POST** /admin/comics | Create a new comic
*AdministrationApi* | [**adminCreateGenre**](docs/AdministrationApi.md#admincreategenreoperation) | **POST** /admin/genres | Create a new genre
*AdministrationApi* | [**adminCreateUser**](docs/AdministrationApi.md#admincreateuseroperation) | **POST** /admin/users | Create new user account (Admin only)
*AdministrationApi* | [**adminDeleteChapter**](docs/AdministrationApi.md#admindeletechapter) | **DELETE** /admin/chapters/{id} | Delete chapter by ID
*AdministrationApi* | [**adminDeleteComic**](docs/AdministrationApi.md#admindeletecomic) | **DELETE** /admin/comics/{id} | Delete comic by ID
*AdministrationApi* | [**adminDeleteGenre**](docs/AdministrationApi.md#admindeletegenre) | **DELETE** /admin/genres/{id} | Delete genre (Admin only)
*AdministrationApi* | [**adminDeleteUser**](docs/AdministrationApi.md#admindeleteuser) | **DELETE** /admin/users/{id} | Delete user account (Admin only)
*AdministrationApi* | [**adminGetStats**](docs/AdministrationApi.md#admingetstats) | **GET** /admin/stats | System overview stats (Admin only)
*AdministrationApi* | [**adminListUsers**](docs/AdministrationApi.md#adminlistusers) | **GET** /admin/users | List registered users (Admin only)
*AdministrationApi* | [**adminUpdateComic**](docs/AdministrationApi.md#adminupdatecomicoperation) | **PUT** /admin/comics/{id} | Update comic by ID
*AdministrationApi* | [**adminUpdateGenre**](docs/AdministrationApi.md#adminupdategenreoperation) | **PUT** /admin/genres/{id} | Update genre by ID
*AdministrationApi* | [**adminUpdateUser**](docs/AdministrationApi.md#adminupdateuseroperation) | **PUT** /admin/users/{id} | Update user account (Admin only)
*BookmarksApi* | [**deleteBookmark**](docs/BookmarksApi.md#deletebookmark) | **DELETE** /bookmarks/{comicId} | Remove comic bookmark
*BookmarksApi* | [**listBookmarks**](docs/BookmarksApi.md#listbookmarks) | **GET** /bookmarks | List user bookmarks
*BookmarksApi* | [**upsertBookmark**](docs/BookmarksApi.md#upsertbookmarkoperation) | **POST** /bookmarks | Add or update comic bookmark
*ChaptersApi* | [**getChapterReaderPages**](docs/ChaptersApi.md#getchapterreaderpages) | **GET** /comics/{comicSlug}/chapters/{chapterSlug} | Get chapter reader pages and navigation
*ComicsApi* | [**getComicBySlug**](docs/ComicsApi.md#getcomicbyslug) | **GET** /comics/{slug} | Get comic details by slug
*ComicsApi* | [**getTrendingComics**](docs/ComicsApi.md#gettrendingcomics) | **GET** /comics/trending | Get trending comics
*ComicsApi* | [**listComics**](docs/ComicsApi.md#listcomics) | **GET** /comics | List and filter comics
*CommentsApi* | [**createComment**](docs/CommentsApi.md#createcommentoperation) | **POST** /comments | Post a comment or reply
*CommentsApi* | [**deleteComment**](docs/CommentsApi.md#deletecomment) | **DELETE** /comments/{id} | Delete comment
*CommentsApi* | [**listComments**](docs/CommentsApi.md#listcomments) | **GET** /comments | List comments for comic or chapter
*CommentsApi* | [**reportComment**](docs/CommentsApi.md#reportcommentoperation) | **POST** /comments/{id}/report | Report an inappropriate comment
*CommentsApi* | [**toggleCommentLike**](docs/CommentsApi.md#togglecommentlike) | **POST** /comments/{id}/like | Toggle like on comment
*GenresApi* | [**listGenres**](docs/GenresApi.md#listgenres) | **GET** /genres | List all comic genres
*HealthApi* | [**getHealthStatus**](docs/HealthApi.md#gethealthstatus) | **GET** /health | Service health and runtime environment check
*ModerationApi* | [**adminListReports**](docs/ModerationApi.md#adminlistreports) | **GET** /admin/reports | List user reports (Admin only)
*ModerationApi* | [**adminUpdateReport**](docs/ModerationApi.md#adminupdatereportoperation) | **PATCH** /admin/reports/{id} | Update report status (Admin only)
*RatingsApi* | [**getComicRating**](docs/RatingsApi.md#getcomicrating) | **GET** /ratings/{comicId} | Get comic rating stats and user rating
*RatingsApi* | [**upsertComicRating**](docs/RatingsApi.md#upsertcomicratingoperation) | **POST** /ratings | Rate a comic
*ReadingHistoryApi* | [**deleteReadingHistory**](docs/ReadingHistoryApi.md#deletereadinghistory) | **DELETE** /history/{comicId} | Clear reading history for comic
*ReadingHistoryApi* | [**listReadingHistory**](docs/ReadingHistoryApi.md#listreadinghistory) | **GET** /history | List user reading history
*ReadingHistoryApi* | [**recordReadingHistory**](docs/ReadingHistoryApi.md#recordreadinghistoryoperation) | **POST** /history | Record chapter reading progress
*SearchApi* | [**getSearchSuggestions**](docs/SearchApi.md#getsearchsuggestions) | **GET** /search/suggest | Instant search autocomplete suggestions
*SearchApi* | [**searchComics**](docs/SearchApi.md#searchcomics) | **GET** /search | Full text comic search
*SitemapsApi* | [**getComicSitemapXml**](docs/SitemapsApi.md#getcomicsitemapxml) | **GET** /sitemap | XML sitemap generator
*SystemApi* | [**clearSystemCache**](docs/SystemApi.md#clearsystemcache) | **POST** /admin/system/clear-cache | Clear search cache (Admin only)
*SystemApi* | [**getSystemStatus**](docs/SystemApi.md#getsystemstatus) | **GET** /admin/system/status | System infrastructure status (Admin only)
*SystemApi* | [**purgeSystemStorage**](docs/SystemApi.md#purgesystemstorage) | **POST** /admin/system/purge-storage | Purge orphan files from R2 storage (Admin only)
*SystemApi* | [**syncSystemViews**](docs/SystemApi.md#syncsystemviews) | **POST** /admin/system/sync-views | Manually trigger view sync and rankings refresh (Admin only)
*UsersApi* | [**deleteOwnAccount**](docs/UsersApi.md#deleteownaccountoperation) | **DELETE** /users/profile | Delete own account
*UsersApi* | [**getUserProfile**](docs/UsersApi.md#getuserprofile) | **GET** /users/profile | Get current user profile
*UsersApi* | [**uploadUserAvatar**](docs/UsersApi.md#uploaduseravatar) | **POST** /users/avatar | Upload profile avatar image
*ViewsApi* | [**recordComicView**](docs/ViewsApi.md#recordcomicviewoperation) | **POST** /view | Record comic/chapter view


### Models

- [AdminCreateChapter200Response](docs/AdminCreateChapter200Response.md)
- [AdminCreateChapterPages200Response](docs/AdminCreateChapterPages200Response.md)
- [AdminCreateChapterPages200ResponseData](docs/AdminCreateChapterPages200ResponseData.md)
- [AdminCreateChapterPagesRequest](docs/AdminCreateChapterPagesRequest.md)
- [AdminCreateChapterPagesRequestPagesInner](docs/AdminCreateChapterPagesRequestPagesInner.md)
- [AdminCreateChapterRequest](docs/AdminCreateChapterRequest.md)
- [AdminCreateComicRequest](docs/AdminCreateComicRequest.md)
- [AdminCreateGenreRequest](docs/AdminCreateGenreRequest.md)
- [AdminCreateUserRequest](docs/AdminCreateUserRequest.md)
- [AdminGetStats200Response](docs/AdminGetStats200Response.md)
- [AdminGetStats200ResponseData](docs/AdminGetStats200ResponseData.md)
- [AdminListReports200Response](docs/AdminListReports200Response.md)
- [AdminListReports200ResponseDataInner](docs/AdminListReports200ResponseDataInner.md)
- [AdminListUsers200Response](docs/AdminListUsers200Response.md)
- [AdminListUsers200ResponseData](docs/AdminListUsers200ResponseData.md)
- [AdminUpdateComic200Response](docs/AdminUpdateComic200Response.md)
- [AdminUpdateComicRequest](docs/AdminUpdateComicRequest.md)
- [AdminUpdateGenre200Response](docs/AdminUpdateGenre200Response.md)
- [AdminUpdateGenreRequest](docs/AdminUpdateGenreRequest.md)
- [AdminUpdateReport200Response](docs/AdminUpdateReport200Response.md)
- [AdminUpdateReport200ResponseData](docs/AdminUpdateReport200ResponseData.md)
- [AdminUpdateReportRequest](docs/AdminUpdateReportRequest.md)
- [AdminUpdateUser200Response](docs/AdminUpdateUser200Response.md)
- [AdminUpdateUserRequest](docs/AdminUpdateUserRequest.md)
- [Bookmark](docs/Bookmark.md)
- [Chapter](docs/Chapter.md)
- [ChapterPage](docs/ChapterPage.md)
- [ClearSystemCache200Response](docs/ClearSystemCache200Response.md)
- [ClearSystemCache200ResponseData](docs/ClearSystemCache200ResponseData.md)
- [Comic](docs/Comic.md)
- [ComicDetail](docs/ComicDetail.md)
- [ComicDetailCreatorsInner](docs/ComicDetailCreatorsInner.md)
- [ComicGenresInner](docs/ComicGenresInner.md)
- [ComicRating](docs/ComicRating.md)
- [Comment](docs/Comment.md)
- [CommentUser](docs/CommentUser.md)
- [CreateComment200Response](docs/CreateComment200Response.md)
- [CreateCommentRequest](docs/CreateCommentRequest.md)
- [DeleteOwnAccountRequest](docs/DeleteOwnAccountRequest.md)
- [ErrorResponse](docs/ErrorResponse.md)
- [Genre](docs/Genre.md)
- [GetChapterReaderPages200Response](docs/GetChapterReaderPages200Response.md)
- [GetChapterReaderPages200ResponseData](docs/GetChapterReaderPages200ResponseData.md)
- [GetChapterReaderPages200ResponseDataPrevChapter](docs/GetChapterReaderPages200ResponseDataPrevChapter.md)
- [GetComicBySlug200Response](docs/GetComicBySlug200Response.md)
- [GetComicRating200Response](docs/GetComicRating200Response.md)
- [GetHealthStatus200Response](docs/GetHealthStatus200Response.md)
- [GetHealthStatus200ResponseBindings](docs/GetHealthStatus200ResponseBindings.md)
- [GetHealthStatus200ResponseDatabase](docs/GetHealthStatus200ResponseDatabase.md)
- [GetHealthStatus200ResponseNodeCompat](docs/GetHealthStatus200ResponseNodeCompat.md)
- [GetSearchSuggestions200Response](docs/GetSearchSuggestions200Response.md)
- [GetSearchSuggestions200ResponseDataInner](docs/GetSearchSuggestions200ResponseDataInner.md)
- [GetSystemStatus200Response](docs/GetSystemStatus200Response.md)
- [GetSystemStatus200ResponseData](docs/GetSystemStatus200ResponseData.md)
- [GetTrendingComics200Response](docs/GetTrendingComics200Response.md)
- [ListBookmarks200Response](docs/ListBookmarks200Response.md)
- [ListComics200Response](docs/ListComics200Response.md)
- [ListComics200ResponseData](docs/ListComics200ResponseData.md)
- [ListComments200Response](docs/ListComments200Response.md)
- [ListGenres200Response](docs/ListGenres200Response.md)
- [ListReadingHistory200Response](docs/ListReadingHistory200Response.md)
- [Pagination](docs/Pagination.md)
- [PurgeSystemStorage200Response](docs/PurgeSystemStorage200Response.md)
- [PurgeSystemStorage200ResponseData](docs/PurgeSystemStorage200ResponseData.md)
- [ReadingHistory](docs/ReadingHistory.md)
- [RecordComicView200Response](docs/RecordComicView200Response.md)
- [RecordComicViewRequest](docs/RecordComicViewRequest.md)
- [RecordReadingHistory200Response](docs/RecordReadingHistory200Response.md)
- [RecordReadingHistoryRequest](docs/RecordReadingHistoryRequest.md)
- [ReportCommentRequest](docs/ReportCommentRequest.md)
- [SuccessResponse](docs/SuccessResponse.md)
- [SyncSystemViews200Response](docs/SyncSystemViews200Response.md)
- [SyncSystemViews200ResponseData](docs/SyncSystemViews200ResponseData.md)
- [ToggleCommentLike200Response](docs/ToggleCommentLike200Response.md)
- [ToggleCommentLike200ResponseData](docs/ToggleCommentLike200ResponseData.md)
- [UploadUserAvatar200Response](docs/UploadUserAvatar200Response.md)
- [UploadUserAvatar200ResponseData](docs/UploadUserAvatar200ResponseData.md)
- [UpsertBookmark200Response](docs/UpsertBookmark200Response.md)
- [UpsertBookmarkRequest](docs/UpsertBookmarkRequest.md)
- [UpsertComicRatingRequest](docs/UpsertComicRatingRequest.md)
- [UserProfile](docs/UserProfile.md)

### Authorization


Authentication schemes defined for the API:
<a id="SessionCookie"></a>
#### SessionCookie


- **Type**: API key
- **API key parameter name**: `komikhq.session_token`
- **Location**: 
<a id="BearerToken"></a>
#### BearerToken


- **Type**: HTTP Bearer Token authentication

## About

This TypeScript SDK client supports the [Fetch API](https://fetch.spec.whatwg.org/).

Maintained by the KomikHQ Platform Team.

- API version: `1.0.0`
- Package version: `1.2.0`

The generated npm module supports the following:

- Environments
  * Node.js
  * Webpack
  * Browserify
- Language levels
  * ES5 - you must have a Promises/A+ library installed
  * ES6
- Module systems
  * CommonJS
  * ES6 module system


## Development

### Building

To build the TypeScript source code, you need to have Node.js and npm installed.
After cloning the repository, navigate to the project directory and run:

```bash
npm install
npm run build
```

### Publishing

Once you've built the package, you can publish it to npm:

```bash
npm publish
```

## License

[]()
