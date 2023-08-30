This repository contains _decrypted_ flatbuffer dumps of the models involved in the RPC layer of Pokémon GO.

They have been dumped on an iPhone X running game version 0.279.3 on iOS16.3.1, somewhere in Japan; both the request and the response blobs contain a single action proto, which is `METHOD_GET_MAP_OBJECTS` .

All models have been reverse-engineered but I currently don't have any plans to share them with the general public; that being said, these dumps should be enough for you to achieve the same.

### RpcRequest
`RpcRequest` objects contain information such as RpcId, action/platform requests and so on (see  [RequestEnvelope](https://github.com/AeonLucid/POGOProtos/blob/master/src/POGOProtos/Networking/Envelopes/RequestEnvelope.proto)).
They also contains an encrypted device `Signature` and matching nonce to perform decryption; the decrypted Signature is also available in this repository.

### Signature
`Signature` objects contain information such as device, location and sensor data (see [Signature](https://github.com/AeonLucid/POGOProtos/blob/master/src/POGOProtos/Networking/Envelopes/Signature.proto)).

### RpcResponse
`RpcResponse` objects contain information such as RpcId, action/platform responses and status code (see [ResponseEnvelope](https://github.com/AeonLucid/POGOProtos/blob/master/src/POGOProtos/Networking/Envelopes/ResponseEnvelope.proto)).
