# Change Log

## 3.7.0

### Added

- Added tag Rooms / Groups
- Added AI endpoints: resolve a pending editor file-generation tool (`POST /ai/chats/tool-files/{callId}/decision`), get and update per-user AI settings (`GET`/`PUT /ai/config/user`)
- Added filling forms room external DB sync endpoints: get sync status and start sync (`GET`/`POST /files/rooms/{id}/externaldbsync`)
- Added payment endpoints for AI balance: credit AI balance (`POST /portal/payment/creditaibalance`) and get the customer AI balance (`GET /portal/payment/customer/aibalance`)
- Added `PUT /files/settings/externalsharingsettings` to change the Access Control external sharing settings
- Added `sendFormToExternalDB` and `saveFormAsXLSX` properties to the room creation request
- Added `withSubFolders` query parameter to folder content listing

### Changed

- Updated SDK OpenAPI specification v3.7.0 (regenerated via OpenAPI Generator)
- File upload now uses `multipart/form-data`, with `createNewIfExist`, `storeOriginalFile`, and `keepConvertStatus` moved to query parameters
- Renamed "Get TFA confirmation URL" to "Get TFA confirmation data"
- Wallet payment amount calculation moved to `PUT /portal/payment/calculatewallet` and the checkout setup URL now accepts `successUrl`
- Payment history filters changed from list types (`types`, `status`) to single-value (`type`), and dropped the `writeOffServiceQuota` parameter
- Updated method descriptions (user existence check, password recovery with CAPTCHA note, webhook triggers) and example values

### Removed

- Removed `POST /portal/payment/buywalletservice` (buy wallet service)
- Removed `GET /portal/payment/customer/servicequota` (get the service quota)

### Fixed

- Fixed & / ' issues

## 3.6.0

- Initial release
- SDK regenerated from OpenAPI specification v3.6.0