# capacitor-google-pay

Google Pay In-App Provisioning

## Install

```bash
npm install capacitor-google-pay
npx cap sync
```

## API

<docgen-index>

* [`addListener('registerDataChangedListener', ...)`](#addlistenerregisterdatachangedlistener)
* [`removeAllListeners()`](#removealllisteners)
* [`getEnvironment()`](#getenvironment)
* [`getStableHardwareId()`](#getstablehardwareid)
* [`getActiveWalletID()`](#getactivewalletid)
* [`getTokenStatus(...)`](#gettokenstatus)
* [`listTokens()`](#listtokens)
* [`isTokenized(...)`](#istokenized)
* [`pushProvision(...)`](#pushprovision)
* [`requestDeleteToken(...)`](#requestdeletetoken)
* [`registerDataChangedListener()`](#registerdatachangedlistener)
* [Interfaces](#interfaces)

</docgen-index>

<docgen-api>
<!--Update the source file JSDoc comments and rerun docgen to update the docs below-->

### addListener('registerDataChangedListener', ...)

```typescript
addListener(eventName: 'registerDataChangedListener', listenerFunc: (response: any) => void) => PluginListenerHandle
```

Event called when an action is performed on a pusn notification.

| Param              | Type                                       | Description                            |
| ------------------ | ------------------------------------------ | -------------------------------------- |
| **`eventName`**    | <code>'registerDataChangedListener'</code> | pushNotificationActionPerformed.       |
| **`listenerFunc`** | <code>(response: any) =&gt; void</code>    | callback with the notification action. |

**Returns:** <code><a href="#pluginlistenerhandle">PluginListenerHandle</a></code>

**Since:** 1.0.0

--------------------


### removeAllListeners()

```typescript
removeAllListeners() => void
```

--------------------


### getEnvironment()

```typescript
getEnvironment() => any
```

returns the environment (e.g. production or sandbox)

**Returns:** <code>any</code>

**Since:** 1.0.0

--------------------


### getStableHardwareId()

```typescript
getStableHardwareId() => any
```

returns the stable hardware ID of the device

**Returns:** <code>any</code>

**Since:** 1.0.0

--------------------


### getActiveWalletID()

```typescript
getActiveWalletID() => any
```

returns the ID of the active wallet

**Returns:** <code>any</code>

**Since:** 1.0.0

--------------------


### getTokenStatus(...)

```typescript
getTokenStatus(options: GooglePayTokenOptions) => any
```

returns the status of a token with a given token ID

| Param         | Type                                                                    | Description   |
| ------------- | ----------------------------------------------------------------------- | ------------- |
| **`options`** | <code><a href="#googlepaytokenoptions">GooglePayTokenOptions</a></code> | Token Options |

**Returns:** <code>any</code>

**Since:** 1.0.0

--------------------


### listTokens()

```typescript
listTokens() => any
```

returns a list of tokens registered to the active wallet

**Returns:** <code>any</code>

**Since:** 1.0.0

--------------------


### isTokenized(...)

```typescript
isTokenized(options: GooglePayIsTokenizedOptions) => any
```

Starts the push tokenization flow

| Param         | Type                                                                                |
| ------------- | ----------------------------------------------------------------------------------- |
| **`options`** | <code><a href="#googlepayistokenizedoptions">GooglePayIsTokenizedOptions</a></code> |

**Returns:** <code>any</code>

**Since:** 1.0.0

--------------------


### pushProvision(...)

```typescript
pushProvision(options: GooglePayProvisionOptions) => any
```

Starts the push tokenization flow

| Param         | Type                                                                            |
| ------------- | ------------------------------------------------------------------------------- |
| **`options`** | <code><a href="#googlepayprovisionoptions">GooglePayProvisionOptions</a></code> |

**Returns:** <code>any</code>

**Since:** 1.0.0

--------------------


### requestDeleteToken(...)

```typescript
requestDeleteToken(options: GooglePayTokenOptions) => any
```

Starts the push tokenization flow

| Param         | Type                                                                    | Description   |
| ------------- | ----------------------------------------------------------------------- | ------------- |
| **`options`** | <code><a href="#googlepaytokenoptions">GooglePayTokenOptions</a></code> | Token Options |

**Returns:** <code>any</code>

**Since:** 1.0.0

--------------------


### registerDataChangedListener()

```typescript
registerDataChangedListener() => any
```

returns the status of a token with a given token ID

**Returns:** <code>any</code>

**Since:** 1.0.0

--------------------


### Interfaces


#### PluginListenerHandle

| Prop         | Type                      |
| ------------ | ------------------------- |
| **`remove`** | <code>() =&gt; any</code> |


#### GooglePayTokenOptions

| Prop                   | Type                | Description                                                                               | Since |
| ---------------------- | ------------------- | ----------------------------------------------------------------------------------------- | ----- |
| **`tsp`**              | <code>string</code> | Sets the TSP that should be used for the tokenization attempt (see TokenServiceProvider). | 1.0.0 |
| **`tokenReferenceId`** | <code>string</code> | token registered to the active wallet                                                     | 1.0.0 |


#### GooglePayIsTokenizedOptions

| Prop             | Type                | Description                                                                                      | Since |
| ---------------- | ------------------- | ------------------------------------------------------------------------------------------------ | ----- |
| **`tsp`**        | <code>string</code> | Sets the TSP that should be used for the tokenization attempt (see TokenServiceProvider).        | 1.0.0 |
| **`lastDigits`** | <code>string</code> | Sets the lastDigits that should be used for the tokenization attempt (see TokenServiceProvider). | 1.0.0 |


#### GooglePayProvisionOptions

| Prop             | Type                                                | Description                                                                                      | Since |
| ---------------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ----- |
| **`opc`**        | <code>string</code>                                 | Sets Opaque Payment Card binary data.                                                            | 1.0.0 |
| **`tsp`**        | <code>string</code>                                 | Sets the TSP that should be used for the tokenization attempt (see TokenServiceProvider).        | 1.0.0 |
| **`clientName`** | <code>string</code>                                 | Sets the clientName that should be used for the tokenization attempt (see TokenServiceProvider). | 1.0.0 |
| **`lastDigits`** | <code>string</code>                                 | Sets the lastDigits that should be used for the tokenization attempt (see TokenServiceProvider). | 1.0.0 |
| **`address`**    | <code><a href="#gpayaddress">GPayAddress</a></code> | Sets the address that should be used for the tokenization attempt (see TokenServiceProvider).    | 1.0.0 |


#### GPayAddress

| Prop                     | Type                | Description         | Since |
| ------------------------ | ------------------- | ------------------- | ----- |
| **`name`**               | <code>string</code> | Address name        | 1.0.0 |
| **`address1`**           | <code>string</code> | Full address        | 1.0.0 |
| **`address2`**           | <code>string</code> | Apartment/Office    | 1.0.0 |
| **`locality`**           | <code>string</code> | Locality            | 1.0.0 |
| **`administrativeArea`** | <code>string</code> | Administrative area | 1.0.0 |
| **`countryCode`**        | <code>string</code> | Country code        | 1.0.0 |
| **`postalCode`**         | <code>string</code> | Postal code         | 1.0.0 |
| **`phoneNumber`**        | <code>string</code> | Phone number        | 1.0.0 |

</docgen-api>
