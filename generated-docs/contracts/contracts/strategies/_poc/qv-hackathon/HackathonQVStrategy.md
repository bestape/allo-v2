# HackathonQVStrategy









## Methods

### NATIVE

```solidity
function NATIVE() external view returns (address)
```

Address of the native token




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### VERSION

```solidity
function VERSION() external view returns (string)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | undefined |

### _NO_RELATED_ATTESTATION_UID

```solidity
function _NO_RELATED_ATTESTATION_UID() external view returns (bytes32)
```

====================== ====== Storage ======= ======================




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### allocate

```solidity
function allocate(bytes _data, address _sender) external payable
```

Allocates to a recipient.

*The encoded &#39;_data&#39; will be determined by the strategy implementation. Only &#39;Allo&#39; contract can      call this when it is initialized.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _data | bytes | The data to use to allocate to the recipient |
| _sender | address | The address of the sender |

### allocationEndTime

```solidity
function allocationEndTime() external view returns (uint64)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint64 | undefined |

### allocationStartTime

```solidity
function allocationStartTime() external view returns (uint64)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint64 | undefined |

### allocators

```solidity
function allocators(address) external view returns (uint256 voiceCredits)
```

The details of the allocator are returned using their address



#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| voiceCredits | uint256 | undefined |

### attest

```solidity
function attest(Attestation attestation) external payable returns (bool)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| attestation | Attestation | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### distribute

```solidity
function distribute(address[] _recipientIds, bytes _data, address _sender) external nonpayable
```

Distributes funds (tokens) to recipients.

*The encoded &#39;_data&#39; will be determined by the strategy implementation. Only &#39;Allo&#39; contract can      call this when it is initialized.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _recipientIds | address[] | The IDs of the recipients |
| _data | bytes | The data to use to distribute to the recipients |
| _sender | address | The address of the sender |

### easInfo

```solidity
function easInfo() external view returns (contract IEAS eas, contract ISchemaRegistry schemaRegistry, bytes32 schemaUID, string schema, bool revocable)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| eas | contract IEAS | undefined |
| schemaRegistry | contract ISchemaRegistry | undefined |
| schemaUID | bytes32 | undefined |
| schema | string | undefined |
| revocable | bool | undefined |

### getAllo

```solidity
function getAllo() external view returns (contract IAllo)
```

Getter for the &#39;Allo&#39; contract.




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | contract IAllo | The Allo contract |

### getAttestation

```solidity
function getAttestation(bytes32 uid) external view returns (struct Attestation)
```



*Gets an attestation from the EAS contract using the UID*

#### Parameters

| Name | Type | Description |
|---|---|---|
| uid | bytes32 | The UUID of the attestation to get. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | Attestation | undefined |

### getPayouts

```solidity
function getPayouts(address[], bytes[]) external view returns (struct IStrategy.PayoutSummary[])
```

Get the payouts for the recipients



#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address[] | undefined |
| _1 | bytes[] | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | IStrategy.PayoutSummary[] | The payouts as an array of PayoutSummary structs |

### getPoolAmount

```solidity
function getPoolAmount() external view returns (uint256)
```

Getter for the &#39;poolAmount&#39;.




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | The balance of the pool |

### getPoolId

```solidity
function getPoolId() external view returns (uint256)
```

Getter for the &#39;poolId&#39;.




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | The ID of the pool |

### getRecipient

```solidity
function getRecipient(address _recipientId) external view returns (struct QVBaseStrategy.Recipient)
```

Get the recipient



#### Parameters

| Name | Type | Description |
|---|---|---|
| _recipientId | address | ID of the recipient |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | QVBaseStrategy.Recipient | The recipient |

### getRecipientStatus

```solidity
function getRecipientStatus(address _recipientId) external view returns (enum IStrategy.Status)
```

Getter for the status of a recipient.



#### Parameters

| Name | Type | Description |
|---|---|---|
| _recipientId | address | The ID of the recipient |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | enum IStrategy.Status | The status of the recipient |

### getSchema

```solidity
function getSchema(bytes32 uid) external view returns (struct SchemaRecord)
```



*Gets a schema from the SchemaRegistry contract using the UID*

#### Parameters

| Name | Type | Description |
|---|---|---|
| uid | bytes32 | The UID of the schema to get. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | SchemaRecord | undefined |

### getStrategyId

```solidity
function getStrategyId() external view returns (bytes32)
```

Getter for the &#39;strategyId&#39;.




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | The ID of the strategy |

### increasePoolAmount

```solidity
function increasePoolAmount(uint256 _amount) external nonpayable
```

Increases the pool amount.

*Increases the &#39;poolAmount&#39; by &#39;_amount&#39;. Only &#39;Allo&#39; contract can call this.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _amount | uint256 | The amount to increase the pool by |

### indexToRecipientId

```solidity
function indexToRecipientId(uint256) external view returns (address)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### initialize

```solidity
function initialize(uint256 _poolId, bytes _data) external nonpayable
```



*Initializes the strategy*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _poolId | uint256 | The pool ID for this strategy |
| _data | bytes | The data to initialize the strategy with |

### isAttestationExpired

```solidity
function isAttestationExpired(address _recipientId) external view returns (bool)
```

Returns if the attestation is expired or not



#### Parameters

| Name | Type | Description |
|---|---|---|
| _recipientId | address | The recipient ID to check |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### isPayable

```solidity
function isPayable() external pure returns (bool)
```

Returns if this contract is payable or not




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | True if the attestation is payable, false otherwise |

### isPoolActive

```solidity
function isPoolActive() external view returns (bool)
```

Getter for whether or not the pool is active.




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | &#39;true&#39; if the pool is active, otherwise &#39;false&#39; |

### isValidAllocator

```solidity
function isValidAllocator(address _allocator) external view returns (bool)
```

Checks if the &#39;_allocator&#39; is a valid allocator.

*How the allocator is determined is up to the strategy implementation.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _allocator | address | The address to check if it is a valid allocator for the strategy. |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | &#39;true&#39; if the address is a valid allocator, &#39;false&#39; otherwise |

### maxVoiceCreditsPerAllocator

```solidity
function maxVoiceCreditsPerAllocator() external view returns (uint256)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### metadataRequired

```solidity
function metadataRequired() external view returns (bool)
```

Whether or not the strategy requires metadata




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### multiAttest

```solidity
function multiAttest(Attestation[] attestations, uint256[] values) external payable returns (bool)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| attestations | Attestation[] | undefined |
| values | uint256[] | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### multiRevoke

```solidity
function multiRevoke(Attestation[] attestations, uint256[] values) external payable returns (bool)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| attestations | Attestation[] | undefined |
| values | uint256[] | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### nft

```solidity
function nft() external view returns (contract ERC721)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | contract ERC721 | undefined |

### paidOut

```solidity
function paidOut(address) external view returns (bool)
```

Returns whether or not the recipient has been paid out using their ID



#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### payoutPercentages

```solidity
function payoutPercentages(uint256) external view returns (uint256)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### recipientIdToIndex

```solidity
function recipientIdToIndex(address) external view returns (uint256)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### recipientIdToUID

```solidity
function recipientIdToUID(address) external view returns (bytes32)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### recipients

```solidity
function recipients(address) external view returns (uint256 totalVotesReceived, bool useRegistryAnchor, address recipientAddress, struct Metadata metadata, enum IStrategy.Status recipientStatus)
```

The details of the recipient are returned using their ID



#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| totalVotesReceived | uint256 | undefined |
| useRegistryAnchor | bool | undefined |
| recipientAddress | address | undefined |
| metadata | Metadata | undefined |
| recipientStatus | enum IStrategy.Status | undefined |

### registerRecipient

```solidity
function registerRecipient(bytes _data, address _sender) external payable returns (address recipientId)
```

Registers a recipient.

*Registers a recipient and returns the ID of the recipient. The encoded &#39;_data&#39; will be determined by the      strategy implementation. Only &#39;Allo&#39; contract can call this when it is initialized.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _data | bytes | The data to use to register the recipient |
| _sender | address | The address of the sender |

#### Returns

| Name | Type | Description |
|---|---|---|
| recipientId | address | The recipientId |

### registrationEndTime

```solidity
function registrationEndTime() external view returns (uint64)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint64 | undefined |

### registrationStartTime

```solidity
function registrationStartTime() external view returns (uint64)
```

The start and end times for registrations and allocations




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint64 | undefined |

### registryGating

```solidity
function registryGating() external view returns (bool)
```

Whether or not the strategy is using registry gating




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### reviewRecipients

```solidity
function reviewRecipients(address[] _recipientIds, enum IStrategy.Status[] _recipientStatuses) external nonpayable
```

Review recipient(s) application(s)

*You can review multiple recipients at once or just one. This can only be called by a pool manager and      only during active registration.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _recipientIds | address[] | Ids of the recipients |
| _recipientStatuses | enum IStrategy.Status[] | Statuses of the recipients |

### reviewThreshold

```solidity
function reviewThreshold() external view returns (uint256)
```

The number of votes required to review a recipient




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### reviewsByStatus

```solidity
function reviewsByStatus(address, enum IStrategy.Status) external view returns (uint256)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |
| _1 | enum IStrategy.Status | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### revoke

```solidity
function revoke(Attestation attestation) external payable returns (bool)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| attestation | Attestation | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### setAllowedRecipientIds

```solidity
function setAllowedRecipientIds(address[] _recipientIds, uint64 _expirationTime, bytes _data) external nonpayable
```

Set the allowed recipient IDs



#### Parameters

| Name | Type | Description |
|---|---|---|
| _recipientIds | address[] | The recipient IDs to allow |
| _expirationTime | uint64 | The expiration time of the attestation |
| _data | bytes | The data to include in the attestation |

### setPayoutPercentages

```solidity
function setPayoutPercentages(uint256[] _payoutPercentages) external nonpayable
```

Set the winner payoutPercentages per rank



#### Parameters

| Name | Type | Description |
|---|---|---|
| _payoutPercentages | uint256[] | The payoutPercentages to set |

### totalRecipientVotes

```solidity
function totalRecipientVotes() external view returns (uint256)
```

The total number of votes cast for all recipients




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### updatePoolTimestamps

```solidity
function updatePoolTimestamps(uint64 _registrationStartTime, uint64 _registrationEndTime, uint64 _allocationStartTime, uint64 _allocationEndTime) external nonpayable
```

Set the start and end dates for the pool



#### Parameters

| Name | Type | Description |
|---|---|---|
| _registrationStartTime | uint64 | The start time for the registration |
| _registrationEndTime | uint64 | The end time for the registration |
| _allocationStartTime | uint64 | The start time for the allocation |
| _allocationEndTime | uint64 | The end time for the allocation |

### voiceCreditsUsedPerNftId

```solidity
function voiceCreditsUsedPerNftId(uint256) external view returns (uint256)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### votesByRank

```solidity
function votesByRank(uint256) external view returns (uint256)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |



## Events

### Allocated

```solidity
event Allocated(address indexed recipientId, uint256 amount, address token, address sender)
```

Emitted when a recipient is allocated to.



#### Parameters

| Name | Type | Description |
|---|---|---|
| recipientId `indexed` | address | The ID of the recipient |
| amount  | uint256 | The amount allocated |
| token  | address | The token allocated |
| sender  | address | undefined |

### Distributed

```solidity
event Distributed(address indexed recipientId, address recipientAddress, uint256 amount, address sender)
```

Emitted when tokens are distributed.



#### Parameters

| Name | Type | Description |
|---|---|---|
| recipientId `indexed` | address | The ID of the recipient |
| recipientAddress  | address | The recipient |
| amount  | uint256 | The amount distributed |
| sender  | address | The sender |

### Initialized

```solidity
event Initialized(address allo, bytes32 profileId, uint256 poolId, bytes data)
```

Emitted when strategy is initialized.



#### Parameters

| Name | Type | Description |
|---|---|---|
| allo  | address | The Allo contract |
| profileId  | bytes32 | The ID of the profile |
| poolId  | uint256 | The ID of the pool |
| data  | bytes | undefined |

### PoolActive

```solidity
event PoolActive(bool active)
```

Emitted when pool is set to active status.



#### Parameters

| Name | Type | Description |
|---|---|---|
| active  | bool | The status of the pool |

### RecipientStatusUpdated

```solidity
event RecipientStatusUpdated(address indexed recipientId, enum IStrategy.Status status, address sender)
```

Emitted when a recipient is registered



#### Parameters

| Name | Type | Description |
|---|---|---|
| recipientId `indexed` | address | ID of the recipient |
| status  | enum IStrategy.Status | The status of the recipient |
| sender  | address | The sender of the transaction |

### Registered

```solidity
event Registered(address indexed recipientId, bytes data, address sender)
```

Emitted when a recipient is registered.



#### Parameters

| Name | Type | Description |
|---|---|---|
| recipientId `indexed` | address | The ID of the recipient |
| data  | bytes | The data passed to the &#39;registerRecipient&#39; function |
| sender  | address | The sender |

### Reviewed

```solidity
event Reviewed(address indexed recipientId, enum IStrategy.Status status, address sender)
```

Emitted when a recipient is reviewed



#### Parameters

| Name | Type | Description |
|---|---|---|
| recipientId `indexed` | address | ID of the recipient |
| status  | enum IStrategy.Status | The status of the recipient |
| sender  | address | The sender of the transaction |

### TimestampsUpdated

```solidity
event TimestampsUpdated(uint64 registrationStartTime, uint64 registrationEndTime, uint64 allocationStartTime, uint64 allocationEndTime, address sender)
```

Emitted when the pool timestamps are updated



#### Parameters

| Name | Type | Description |
|---|---|---|
| registrationStartTime  | uint64 | The start time for the registration |
| registrationEndTime  | uint64 | The end time for the registration |
| allocationStartTime  | uint64 | The start time for the allocation |
| allocationEndTime  | uint64 | The end time for the allocation |
| sender  | address | The sender of the transaction |

### UpdatedRegistration

```solidity
event UpdatedRegistration(address indexed recipientId, bytes data, address sender, enum IStrategy.Status status)
```

Emitted when a recipient updates their registration



#### Parameters

| Name | Type | Description |
|---|---|---|
| recipientId `indexed` | address | ID of the recipient |
| data  | bytes | The encoded data - (address recipientId, address recipientAddress, Metadata metadata) |
| sender  | address | The sender of the transaction |
| status  | enum IStrategy.Status | The updated status of the recipient |



## Errors

### ALLOCATION_ACTIVE

```solidity
error ALLOCATION_ACTIVE()
```

Thrown when the allocation is active.




### ALLOCATION_NOT_ACTIVE

```solidity
error ALLOCATION_NOT_ACTIVE()
```

Thrown when the allocation is not active.




### ALLOCATION_NOT_ENDED

```solidity
error ALLOCATION_NOT_ENDED()
```

Thrown when the allocation is not ended.




### ALREADY_ADDED

```solidity
error ALREADY_ADDED()
```

====================== ==== Custom Error ==== ======================




### ALREADY_INITIALIZED

```solidity
error ALREADY_INITIALIZED()
```

Thrown when data is already intialized




### AMOUNT_MISMATCH

```solidity
error AMOUNT_MISMATCH()
```

Thrown when the amount of tokens sent does not match the amount of tokens expected




### ANCHOR_ERROR

```solidity
error ANCHOR_ERROR()
```



*Thrown if the anchor creation fails*


### ARRAY_MISMATCH

```solidity
error ARRAY_MISMATCH()
```

Thrown when two arrays length are not equal




### AccessDenied

```solidity
error AccessDenied()
```






### INVALID

```solidity
error INVALID()
```

Thrown as a general error when input / data is invalid




### INVALID_ADDRESS

```solidity
error INVALID_ADDRESS()
```

Thrown when an invalid address is used




### INVALID_FEE

```solidity
error INVALID_FEE()
```

Thrown when the fee is below 1e18 which is the fee percentage denominator




### INVALID_METADATA

```solidity
error INVALID_METADATA()
```

Thrown when the metadata is invalid.




### INVALID_REGISTRATION

```solidity
error INVALID_REGISTRATION()
```

Thrown when the registration is invalid.




### INVALID_SCHEMA

```solidity
error INVALID_SCHEMA()
```






### IS_APPROVED_STRATEGY

```solidity
error IS_APPROVED_STRATEGY()
```

Thrown when the strategy is approved and should be cloned




### InsufficientValue

```solidity
error InsufficientValue()
```






### InvalidEAS

```solidity
error InvalidEAS()
```






### MISMATCH

```solidity
error MISMATCH()
```

Thrown when mismatch in decoding data




### NONCE_NOT_AVAILABLE

```solidity
error NONCE_NOT_AVAILABLE()
```



*Thrown when the nonce passed has been used or not available*


### NOT_APPROVED_STRATEGY

```solidity
error NOT_APPROVED_STRATEGY()
```

Thrown when the strategy is not approved




### NOT_ENOUGH_FUNDS

```solidity
error NOT_ENOUGH_FUNDS()
```

Thrown when not enough funds are available




### NOT_INITIALIZED

```solidity
error NOT_INITIALIZED()
```

Thrown when data is yet to be initialized




### NOT_PENDING_OWNER

```solidity
error NOT_PENDING_OWNER()
```



*Thrown when the &#39;msg.sender&#39; is not the pending owner on ownership transfer*


### NotPayable

```solidity
error NotPayable()
```






### OUT_OF_BOUNDS

```solidity
error OUT_OF_BOUNDS()
```






### POOL_ACTIVE

```solidity
error POOL_ACTIVE()
```

Thrown when a pool is already active




### POOL_INACTIVE

```solidity
error POOL_INACTIVE()
```

Thrown when a pool is inactive




### RECIPIENT_ALREADY_ACCEPTED

```solidity
error RECIPIENT_ALREADY_ACCEPTED()
```

Thrown when recipient is already accepted.




### RECIPIENT_ERROR

```solidity
error RECIPIENT_ERROR(address recipientId)
```

Thrown when there is an error in recipient.



#### Parameters

| Name | Type | Description |
|---|---|---|
| recipientId | address | undefined |

### RECIPIENT_NOT_ACCEPTED

```solidity
error RECIPIENT_NOT_ACCEPTED()
```

Thrown when the recipient is not accepted.




### REGISTRATION_NOT_ACTIVE

```solidity
error REGISTRATION_NOT_ACTIVE()
```

Thrown when registration is not active.




### UNAUTHORIZED

```solidity
error UNAUTHORIZED()
```

Thrown when user is not authorized




### ZERO_ADDRESS

```solidity
error ZERO_ADDRESS()
```

Thrown when address is the zero address





