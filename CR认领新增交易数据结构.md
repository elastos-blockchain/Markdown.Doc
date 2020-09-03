##新增交易数据结构

### 1.CR认领DPOS节点交易

**交易类型： CRDPOSManagement**

| Field                 | Type    | Usage                         |
| --------------------- | ------- | ----------------------------- |
| CRManagementPublicKey | []byte  | 认领者公钥                    |
| CRCommitteeDID        | Uint168 | CR委员的DID                   |
| Signature             | []byte  | CROwner私钥对以上字段生成签名 |

交易结构示例:

```
./ela-cli script -f transaction/crc_claims_dpos_node_tx.lua --crmanagementpublickey 03937bf07da2b84bffb1f5c9f254de4c43cb5b6507cf500675e077ae1bc561839d --crdposprivatekey fa3d20d9a96f3e5cfe2aeaa62756752bca1c24f73107fd761b5c33f76f990ad7 --crcommitteedid ijkfyCiYxa4gp58xRGfoJ2ruhQRdbdmdQn --rpcport 10116 --wallet foundation.dat

Transaction: {
	Hash: 78b99a7e7338901e564f58bbf06d9da1d1f201b9ad16f7c0c30a5f8096a02b89
	Version: 9
	TxType: CRDPOSManagement
	PayloadVersion: 0
	Payload: 2103937bf07da2b84bffb1f5c9f254de4c43cb5b6507cf500675e077ae1bc561839d67b9d2d012795aab279e9141046aba758eb495ee4e40ca5e997552f7fbac21fae186727917bf4064dd37c395edc769153dee2511af5fc221b41512618f705d4e532d685944e8c3b9091da62c14e9848a6c9eeec2f025
	Attributes: []
	Inputs: [{TxID: e04f34305b63d35853d423a81e159d1f61fb2ebff55557ea2913de04d80d8916 Index: 0 Sequence: 4294967295}]
	Outputs: [Output: {
			AssetID: b037db964a231458d2d6ffd5ea18944c4f90e63d547c5d3b9874df66a4ead0a3
			Value: 1.50689932
			OutputLock: 0
			ProgramHash: 21fe52a8b287def246bd774bb3b73373d95d99774c
			Type: 0
			Payload: &{}
		}]
	LockTime: 0
	Programs: [Program: {
		Code: 2103db983dd7ff90332b1a8bb5f1d3726c968ed4bd019e2bc54602b5ff3f05e5c0a3ac
		Parameter: 402ae5b9e1619dc9733ccc3dc6f5a49cb46dd914d591841c56e5ceba456358d6493abf26a13bdc8b49dd63ba1e3c2c7daf50038033fbec04aaa0e22f05b5722e87
		}]
	}


sending 892ba096805f0ac3c0f716adb901f2d1a19d6df0bb584f561e9038737e9ab978
tx send success
```





### 2.NextTurnDPOSInfo交易

**交易类型：NextTurnDPOSInfo**

| 字段           | 类型      | 用途         |
| -------------- | --------- | ------------ |
| WorkingHeight  | Uint32    | 生效高度     |
| CRPublickeys   | [] []byte | CR公钥       |
| DPOSPublicKeys | [] []byte | DPOS节点公钥 |



交易结构示例:

```
Transaction: {
	Hash: dc327a5ef958385a23082e8c73b2fa7c330793ad601587db84ecec3977989b33
	Version: 9
	TxType: CRCProposal
	PayloadVersion: 0
	Payload: 0004033131312102f981e4dae4983a5d284d01609ad735e3242c5672bb2c7bb0018cc36f9ab0c4a51f06ed7688f2b6e445f6579ca802fd1b6425b1e02a1944a8df714301f629363521031e12374bae471aa09ad479f66c2306f4bcc4ca5b754609a82a1839b94b4721b967e7bbc540fab57abb2dc9ba1e6cdbf9ae3979e3cb
	Attributes: []
	Inputs: []
	Outputs: []
	LockTime: 0
	Programs: [Program: {
		Code: 2102f981e4dae4983a5d284d01609ad735e3242c5672bb2c7bb0018cc36f9ab0c4a5ac
		Parameter: 
		}]
	}
```















