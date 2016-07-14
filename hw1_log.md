`$ ./gcoin-cli setgenerate true`
	
	true
`$ ./gcoin-cli getinfo`

	{
	    "version" : 1010200,
	    "protocolversion" : 70002,
	    "walletversion" : 60000,
	    "blocks" : 1,
	    "timeoffset" : 0,
	    "connections" : 1,
	    "proxy" : "",
	    "difficulty" : 0.00024414,
	    "testnet" : false,
	    "keypoololdest" : 1468473311,
	    "keystoresize" : 1,
	    "errors" : ""
	}
`$ ./gcoin-cli mint 1 0`

	e9c922e212ee891a3018906b500bca9b2b3ef6d01def57441732240ad3e9cc8d
`$ ./gcoin-cli getinfo`

	{
	    "version" : 1010200,
	    "protocolversion" : 70002,
	    "walletversion" : 60000,
	    "blocks" : 1,
	    "timeoffset" : 0,
	    "connections" : 1,
	    "proxy" : "",
	    "difficulty" : 0.00024414,
	    "testnet" : false,
	    "keypoololdest" : 1468473323,
	    "keystoresize" : 1,
	    "errors" : ""
	}
`$ ./gcoin-cli getinfo`

	{
	    "version" : 1010200,
	    "protocolversion" : 70002,
	    "walletversion" : 60000,
	    "blocks" : 8,
	    "timeoffset" : 0,
	    "connections" : 1,
	    "proxy" : "",
	    "difficulty" : 0.00024414,
	    "testnet" : false,
	    "keypoololdest" : 1468473324,
	    "keystoresize" : 1,
	    "errors" : ""
	}
`$ ./gcoin-cli getinfo`

	{
	    "version" : 1010200,
	    "protocolversion" : 70002,
	    "walletversion" : 60000,
	    "blocks" : 12,
	    "timeoffset" : 0,
	    "connections" : 1,
	    "proxy" : "",
	    "difficulty" : 0.00024414,
	    "testnet" : false,
	    "keypoololdest" : 1468473325,
	    "keystoresize" : 1,
	    "errors" : ""
	}
`$ ./gcoin-cli getrawtransaction e9c922e212ee891a3018906b500bca9b2b3ef6d01def57441732240ad3e9cc8d 1`

	{
	    "hex" : "01000000010000000000000000000000000000000000000000000000000000000000000000ffffffff4847304402207d778dccd858f3fe39e1b108a78a834eb82e534d5ea69d8e00ca5351a34931a802201c9cca7e71e7196153b454f93c5ed1a63b988dfc17f014519aa213023bbec67b01ffffffff0100e1f50500000000232102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0bac000000000000000001000000",
	    "txid" : "e9c922e212ee891a3018906b500bca9b2b3ef6d01def57441732240ad3e9cc8d",
	    "version" : 1,
	    "locktime" : 0,
	    "type" : "MINT",
	    "size" : 175,
	    "vin" : [
	        {
	            "coinbase" : "47304402207d778dccd858f3fe39e1b108a78a834eb82e534d5ea69d8e00ca5351a34931a802201c9cca7e71e7196153b454f93c5ed1a63b988dfc17f014519aa213023bbec67b01",
	            "scriptSig" : {
	                "asm" : "304402207d778dccd858f3fe39e1b108a78a834eb82e534d5ea69d8e00ca5351a34931a802201c9cca7e71e7196153b454f93c5ed1a63b988dfc17f014519aa213023bbec67b01",
	                "hex" : "47304402207d778dccd858f3fe39e1b108a78a834eb82e534d5ea69d8e00ca5351a34931a802201c9cca7e71e7196153b454f93c5ed1a63b988dfc17f014519aa213023bbec67b01"
	            },
	            "sequence" : 4294967295
	        }
	    ],
	    "vout" : [
	        {
	            "value" : 100000000,
	            "n" : 0,
	            "scriptPubKey" : {
	                "asm" : "02247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b OP_CHECKSIG",
	                "hex" : "2102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0bac",
	                "reqSigs" : 1,
	                "type" : "pubkey",
	                "addresses" : [
	                    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	                ]
	            },
	            "color" : 0
	        }
	    ],
	    "blockhash" : "0000078e74ebd99dc0fd779592bd637abe23b6cb4adce03a64ba002385594911",
	    "confirmations" : 11,
	    "time" : 1468473324,
	    "blocktime" : 1468473324
	}
`$ ./gcoin-cli getaddressbalance 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx`

	{
  	  "0" : 1.00000000
	}
`$ ./gcoin-cli getinfo`

	{
	    "version" : 1010200,
	    "protocolversion" : 70002,
	    "walletversion" : 60000,
	    "blocks" : 12,
	    "timeoffset" : 0,
	    "connections" : 1,
	    "proxy" : "",
	    "difficulty" : 0.00024414,
	    "testnet" : false,
	    "keypoololdest" : 1468473459,
	    "keystoresize" : 1,
	    "errors" : ""
	}
`$ ./gcoin-cli mint 1 0`

	adfbaab95065156d8263bf786d264538f100c3c773e72519de6221252031bcb8
`$ ./gcoin-cli getaddressbalance 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx`

	{
  	  "0" : 2.00000000
	}
`$ ./gcoin-cli mint 100 1`
	
	error: {"code":-4,"message":"license of this color hasn't been generated yet"}
`$ ./gcoin-cli listwalletaddress`

	[
  	  "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	]
`$ ./gcoin-cli getinfo`


	{
	    "version" : 1010200,
	    "protocolversion" : 70002,
	    "walletversion" : 60000,
	    "blocks" : 23,
	    "timeoffset" : 0,
	    "connections" : 1,
	    "proxy" : "",
	    "difficulty" : 0.00024414,
	    "testnet" : false,
	    "keypoololdest" : 1468473653,
	    "keystoresize" : 1,
	    "errors" : ""
	}
`$ ./gcoin-cli keypoolrefill 1`

`$ ./gcoin-cli getinfo`

	{
	    "version" : 1010200,
	    "protocolversion" : 70002,
	    "walletversion" : 60000,
	    "blocks" : 23,
	    "timeoffset" : 0,
	    "connections" : 1,
	    "proxy" : "",
	    "difficulty" : 0.00024414,
	    "testnet" : false,
	    "keypoololdest" : 1468473671,
	    "keystoresize" : 2,
	    "errors" : ""
	}
`$ ./gcoin-cli listwalletaddress`

	[
	    "1AdPe51GSfoqarcHXW19RyQG6svfjA6RTp",
	    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	]
`$ ./gcoin-cli sendlicensetoaddress 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx 1 72110100046e616d6503646573046164647201000000000000000000000000046164647200000000000000000000000001046c696e6b0000000000000000000000000000000000000000000000000000000000000000`

	fc55111b7e99c7aabfcf5761376eb438b7076da7ec96f5e435461f3a3cc6f0b8
`$ ./gcoin-cli getrawtransaction fc55111b7e99c7aabfcf5761376eb438b7076da7ec96f5e435461f3a3cc6f0b8 1`

	{
	    "hex" : "01000000018dcce9d30a2432174457ef1dd0f63e2b9bca0b506b9018301a89ee12e222c9e90000000049483045022100e9a3aaf63ea9b4f862ee4f782e060bef08e1a5830ae566f2741dea0f3bfbc24502201bf0a6372e2210017c9f7a9051b319661308c42e77b3c3f7eea7068142482fc801ffffffff0200e1f505000000001976a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac010000000000000000000000af6a4cac37323131303130303034366536313664363530333634363537333034363136343634373230313030303030303030303030303030303030303030303030303034363136343634373230303030303030303030303030303030303030303030303030313034366336393665366230303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030010000000000000002000000",
	    "txid" : "fc55111b7e99c7aabfcf5761376eb438b7076da7ec96f5e435461f3a3cc6f0b8",
	    "version" : 1,
	    "locktime" : 0,
	    "type" : "LICENSE",
	    "size" : 354,
	    "vin" : [
	        {
	            "txid" : "e9c922e212ee891a3018906b500bca9b2b3ef6d01def57441732240ad3e9cc8d",
	            "vout" : 0,
	            "scriptSig" : {
	                "asm" : "3045022100e9a3aaf63ea9b4f862ee4f782e060bef08e1a5830ae566f2741dea0f3bfbc24502201bf0a6372e2210017c9f7a9051b319661308c42e77b3c3f7eea7068142482fc801",
	                "hex" : "483045022100e9a3aaf63ea9b4f862ee4f782e060bef08e1a5830ae566f2741dea0f3bfbc24502201bf0a6372e2210017c9f7a9051b319661308c42e77b3c3f7eea7068142482fc801"
	            },
	            "sequence" : 4294967295
	        }
	    ],
	    "vout" : [
	        {
	            "value" : 100000000,
	            "n" : 0,
	            "scriptPubKey" : {
	                "asm" : "OP_DUP OP_HASH160 8a6343b0603c3f5b16e812b27f833d591d868ed2 OP_EQUALVERIFY OP_CHECKSIG",
	                "hex" : "76a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac",
	                "reqSigs" : 1,
	                "type" : "pubkeyhash",
	                "addresses" : [
	                    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	                ]
	            },
	            "color" : 1
	        },
	        {
	            "value" : 0,
	            "n" : 1,
	            "scriptPubKey" : {
	                "asm" : "OP_RETURN 37323131303130303034366536313664363530333634363537333034363136343634373230313030303030303030303030303030303030303030303030303034363136343634373230303030303030303030303030303030303030303030303030313034366336393665366230303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030",
	                "hex" : "6a4cac37323131303130303034366536313664363530333634363537333034363136343634373230313030303030303030303030303030303030303030303030303034363136343634373230303030303030303030303030303030303030303030303030313034366336393665366230303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030303030",
	                "type" : "nulldata"
	            },
	            "color" : 1
	        }
	    ],
	    "blockhash" : "0000003a65fd248c9ce8648bd5018a7f6acb36faf9e25f32f6082b97a65cdb09",
	    "confirmations" : 11,
	    "time" : 1468473723,
	    "blocktime" : 1468473723
	}
`$ ./gcoin-cli getrawtransaction e9c922e212ee891a3018906b500bca9b2b3ef6d01def57441732240ad3e9cc8d 1`

	{
	    "hex" : "01000000010000000000000000000000000000000000000000000000000000000000000000ffffffff4847304402207d778dccd858f3fe39e1b108a78a834eb82e534d5ea69d8e00ca5351a34931a802201c9cca7e71e7196153b454f93c5ed1a63b988dfc17f014519aa213023bbec67b01ffffffff0100e1f50500000000232102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0bac000000000000000001000000",
	    "txid" : "e9c922e212ee891a3018906b500bca9b2b3ef6d01def57441732240ad3e9cc8d",
	    "version" : 1,
	    "locktime" : 0,
	    "type" : "MINT",
	    "size" : 175,
	    "vin" : [
	        {
	            "coinbase" : "47304402207d778dccd858f3fe39e1b108a78a834eb82e534d5ea69d8e00ca5351a34931a802201c9cca7e71e7196153b454f93c5ed1a63b988dfc17f014519aa213023bbec67b01",
	            "scriptSig" : {
	                "asm" : "304402207d778dccd858f3fe39e1b108a78a834eb82e534d5ea69d8e00ca5351a34931a802201c9cca7e71e7196153b454f93c5ed1a63b988dfc17f014519aa213023bbec67b01",
	                "hex" : "47304402207d778dccd858f3fe39e1b108a78a834eb82e534d5ea69d8e00ca5351a34931a802201c9cca7e71e7196153b454f93c5ed1a63b988dfc17f014519aa213023bbec67b01"
	            },
	            "sequence" : 4294967295
	        }
	    ],
	    "vout" : [
	        {
	            "value" : 100000000,
	            "n" : 0,
	            "scriptPubKey" : {
	                "asm" : "02247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b OP_CHECKSIG",
	                "hex" : "2102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0bac",
	                "reqSigs" : 1,
	                "type" : "pubkey",
	                "addresses" : [
	                    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	                ]
	            },
	            "color" : 0
	        }
	    ],
	    "blockhash" : "0000078e74ebd99dc0fd779592bd637abe23b6cb4adce03a64ba002385594911",
	    "confirmations" : 33,
	    "time" : 1468473324,
	    "blocktime" : 1468473324
	}
`$ ./gcoin-cli getaddressbalance 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx`

	{
	    "0" : 1.00000000
	}
`$ ./gcoin-cli getlicenseinfo 1`

	{
	    "Owner" : "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx",
	    "Total amount" : 0,
	    "version" : 1,
	    "name" : "name",
	    "description" : "des",
	    "issuer" : "addr",
	    "divisibility" : "true",
	    "fee_type" : "fixed",
	    "fee_rate" : 0.00000000,
	    "fee_collector" : "addr",
	    "upper_limit" : 0,
	    "mint_schedule" : "free",
	    "member_control" : "true",
	    "metadata_link" : "link",
	    "metadata_hash" : "0000000000000000000000000000000000000000000000000000000000000000"
	}
`$ ./gcoin-cli mint 100 1`

	7bcb808fae76950eb9803a962a53ef0486c40870990d291595a3bbf730e0b94d
`$ ./gcoin-cli getrawtransaction 7bcb808fae76950eb9803a962a53ef0486c40870990d291595a3bbf730e0b94d 1`

	{
	    "hex" : "01000000010000000000000000000000000000000000000000000000000000000000000000ffffffff6b483045022100b7e308b6f1dfc82001f5a87b277d7020905f6a1047de35b82aca0d427a51af650220182c908eb8dfc8d16fe492125e338ab5e2d79bd3b21d24fa67d8a581b921dadb012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0bffffffff0100e40b54020000001976a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac010000000000000001000000",
	    "txid" : "7bcb808fae76950eb9803a962a53ef0486c40870990d291595a3bbf730e0b94d",
	    "version" : 1,
	    "locktime" : 0,
	    "type" : "MINT",
	    "size" : 200,
	    "vin" : [
	        {
	            "coinbase" : "483045022100b7e308b6f1dfc82001f5a87b277d7020905f6a1047de35b82aca0d427a51af650220182c908eb8dfc8d16fe492125e338ab5e2d79bd3b21d24fa67d8a581b921dadb012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b",
	            "scriptSig" : {
	                "asm" : "3045022100b7e308b6f1dfc82001f5a87b277d7020905f6a1047de35b82aca0d427a51af650220182c908eb8dfc8d16fe492125e338ab5e2d79bd3b21d24fa67d8a581b921dadb01 02247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b",
	                "hex" : "483045022100b7e308b6f1dfc82001f5a87b277d7020905f6a1047de35b82aca0d427a51af650220182c908eb8dfc8d16fe492125e338ab5e2d79bd3b21d24fa67d8a581b921dadb012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b"
	            },
	            "sequence" : 4294967295
	        }
	    ],
	    "vout" : [
	        {
	            "value" : 10000000000,
	            "n" : 0,
	            "scriptPubKey" : {
	                "asm" : "OP_DUP OP_HASH160 8a6343b0603c3f5b16e812b27f833d591d868ed2 OP_EQUALVERIFY OP_CHECKSIG",
	                "hex" : "76a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac",
	                "reqSigs" : 1,
	                "type" : "pubkeyhash",
	                "addresses" : [
	                    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	                ]
	            },
	            "color" : 1
	        }
	    ],
	    "blockhash" : "00000310bf5382e4f07bb49f7f71acc4cd060bd20542551bbe6bde4874a10e0f",
	    "confirmations" : 11,
	    "time" : 1468473988,
	    "blocktime" : 1468473988
	}
`$ ./gcoin-cli getaddressbalance 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx`

	{
	    "0" : 1.00000000,
	    "1" : 100.00000000
	}
`$ ./gcoin-cli sendlicensetoaddress 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx 2 72110100046e616d6503646573046164647201000000000000000000000000046164647200000000000000000000000001046c696e6b0000000000000000000000000000000000000000000000000000000000000000`

	14057cdaf79953afe7e02233cc6d0966196a44a91e60e503a20a9dffe36f328a

`$ ./gcoin-cli getaddressbalance 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx`

	{
	    "1" : 100.00000000
	}
`$ ./gcoin-cli mint 100 2`
	
	ff7ceb320c19a7808f1638d84578d2838bc15c4a98385332314090a652eeae21
`$ ./gcoin-cli getaddressbalance 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx`

	{
	    "1" : 100.00000000
	}
	
`$ ./gcoin-cli getaddressbalance 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx`

	{
	    "1" : 100.00000000,
	    "2" : 100.00000000
	}
`$ ./gcoin-cli getrawtransaction 7bcb808fae76950eb9803a962a53ef0486c40870990d291595a3bbf730e0b94d 1`

	{
	    "hex" : "01000000010000000000000000000000000000000000000000000000000000000000000000ffffffff6b483045022100b7e308b6f1dfc82001f5a87b277d7020905f6a1047de35b82aca0d427a51af650220182c908eb8dfc8d16fe492125e338ab5e2d79bd3b21d24fa67d8a581b921dadb012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0bffffffff0100e40b54020000001976a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac010000000000000001000000",
	    "txid" : "7bcb808fae76950eb9803a962a53ef0486c40870990d291595a3bbf730e0b94d",
	    "version" : 1,
	    "locktime" : 0,
	    "type" : "MINT",
	    "size" : 200,
	    "vin" : [
	        {
	            "coinbase" : "483045022100b7e308b6f1dfc82001f5a87b277d7020905f6a1047de35b82aca0d427a51af650220182c908eb8dfc8d16fe492125e338ab5e2d79bd3b21d24fa67d8a581b921dadb012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b",
	            "scriptSig" : {
	                "asm" : "3045022100b7e308b6f1dfc82001f5a87b277d7020905f6a1047de35b82aca0d427a51af650220182c908eb8dfc8d16fe492125e338ab5e2d79bd3b21d24fa67d8a581b921dadb01 02247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b",
	                "hex" : "483045022100b7e308b6f1dfc82001f5a87b277d7020905f6a1047de35b82aca0d427a51af650220182c908eb8dfc8d16fe492125e338ab5e2d79bd3b21d24fa67d8a581b921dadb012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b"
	            },
	            "sequence" : 4294967295
	        }
	    ],
	    "vout" : [
	        {
	            "value" : 10000000000,
	            "n" : 0,
	            "scriptPubKey" : {
	                "asm" : "OP_DUP OP_HASH160 8a6343b0603c3f5b16e812b27f833d591d868ed2 OP_EQUALVERIFY OP_CHECKSIG",
	                "hex" : "76a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac",
	                "reqSigs" : 1,
	                "type" : "pubkeyhash",
	                "addresses" : [
	                    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	                ]
	            },
	            "color" : 1
	        }
	    ],
	    "blockhash" : "00000310bf5382e4f07bb49f7f71acc4cd060bd20542551bbe6bde4874a10e0f",
	    "confirmations" : 33,
	    "time" : 1468473988,
	    "blocktime" : 1468473988
	}
`$ ./gcoin-cli getaddressbalance 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx`

	{
	    "1" : 100.00000000,
	    "2" : 100.00000000
	}
`$ ./gcoin-cli getrawtransaction ff7ceb320c19a7808f1638d84578d2838bc15c4a98385332314090a652eeae21 1`

	{
	    "hex" : "01000000010000000000000000000000000000000000000000000000000000000000000000ffffffff6a473044022018bf2ba6731a685f70f97a9e541fc50adcb682da782647d52b9a33cfeac5761e022006bae3ed981fe8789275e1ff08aa91cc74f0787fe0a7ae59606223badcc1ac2e012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0bffffffff0100e40b54020000001976a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac020000000000000001000000",
	    "txid" : "ff7ceb320c19a7808f1638d84578d2838bc15c4a98385332314090a652eeae21",
	    "version" : 1,
	    "locktime" : 0,
	    "type" : "MINT",
	    "size" : 199,
	    "vin" : [
	        {
	            "coinbase" : "473044022018bf2ba6731a685f70f97a9e541fc50adcb682da782647d52b9a33cfeac5761e022006bae3ed981fe8789275e1ff08aa91cc74f0787fe0a7ae59606223badcc1ac2e012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b",
	            "scriptSig" : {
	                "asm" : "3044022018bf2ba6731a685f70f97a9e541fc50adcb682da782647d52b9a33cfeac5761e022006bae3ed981fe8789275e1ff08aa91cc74f0787fe0a7ae59606223badcc1ac2e01 02247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b",
	                "hex" : "473044022018bf2ba6731a685f70f97a9e541fc50adcb682da782647d52b9a33cfeac5761e022006bae3ed981fe8789275e1ff08aa91cc74f0787fe0a7ae59606223badcc1ac2e012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b"
	            },
	            "sequence" : 4294967295
	        }
	    ],
	    "vout" : [
	        {
	            "value" : 10000000000,
	            "n" : 0,
	            "scriptPubKey" : {
	                "asm" : "OP_DUP OP_HASH160 8a6343b0603c3f5b16e812b27f833d591d868ed2 OP_EQUALVERIFY OP_CHECKSIG",
	                "hex" : "76a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac",
	                "reqSigs" : 1,
	                "type" : "pubkeyhash",
	                "addresses" : [
	                    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	                ]
	            },
	            "color" : 2
	        }
	    ],
	    "blockhash" : "0000059954e98161f4b75e2a5b8ec09364485a6b7ec46d7b87b66f7ca632e16c",
	    "confirmations" : 11,
	    "time" : 1468474086,
	    "blocktime" : 1468474086
	}
`$ ./gcoin-cli sendtoaddress 1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx 40 2`

	208552cc4a94af817fae5922952be6ae9a9f2d69c48042f5eced5fe8e2e4c6e2
`$ ./gcoin-cli getrawtransaction 208552cc4a94af817fae5922952be6ae9a9f2d69c48042f5eced5fe8e2e4c6e2 1`

	{
	    "hex" : "01000000024db9e030f7bba39515290d997008c48604ef532a963a80b90e9576ae8f80cb7b000000006b4830450221008907815392e0feca44ea6f09e1d283920512a231ce1b15e9abe10a8a1aa3049a02201d2dc595a1b65948884c5a058e6eb4735e812ff39c4e90146fae6984f4175f30012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0bfeffffff21aeee52a6904031325338984a5cc18b83d27845d838168f80a7190c32eb7cff000000006a473044022037145fec8df7d09be5ba276278a2885eabd3d3609aa3e43aeed34f7c0bb8c07d02205f55729d7dc72896677f6b6f4e4cb16a02de6b9594fed0115bcfac5625c055a3012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0bfeffffff0300286bee000000001976a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac0200000000bca065010000001976a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac020000000003164e020000001976a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac010000003900000000000000",
	    "txid" : "208552cc4a94af817fae5922952be6ae9a9f2d69c48042f5eced5fe8e2e4c6e2",
	    "version" : 1,
	    "locktime" : 57,
	    "type" : "NORMAL",
	    "size" : 423,
	    "vin" : [
	        {
	            "txid" : "7bcb808fae76950eb9803a962a53ef0486c40870990d291595a3bbf730e0b94d",
	            "vout" : 0,
	            "scriptSig" : {
	                "asm" : "30450221008907815392e0feca44ea6f09e1d283920512a231ce1b15e9abe10a8a1aa3049a02201d2dc595a1b65948884c5a058e6eb4735e812ff39c4e90146fae6984f4175f3001 02247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b",
	                "hex" : "4830450221008907815392e0feca44ea6f09e1d283920512a231ce1b15e9abe10a8a1aa3049a02201d2dc595a1b65948884c5a058e6eb4735e812ff39c4e90146fae6984f4175f30012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b"
	            },
	            "sequence" : 4294967294
	        },
	        {
	            "txid" : "ff7ceb320c19a7808f1638d84578d2838bc15c4a98385332314090a652eeae21",
	            "vout" : 0,
	            "scriptSig" : {
	                "asm" : "3044022037145fec8df7d09be5ba276278a2885eabd3d3609aa3e43aeed34f7c0bb8c07d02205f55729d7dc72896677f6b6f4e4cb16a02de6b9594fed0115bcfac5625c055a301 02247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b",
	                "hex" : "473044022037145fec8df7d09be5ba276278a2885eabd3d3609aa3e43aeed34f7c0bb8c07d02205f55729d7dc72896677f6b6f4e4cb16a02de6b9594fed0115bcfac5625c055a3012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b"
	            },
	            "sequence" : 4294967294
	        }
	    ],
	    "vout" : [
	        {
	            "value" : 4000000000,
	            "n" : 0,
	            "scriptPubKey" : {
	                "asm" : "OP_DUP OP_HASH160 8a6343b0603c3f5b16e812b27f833d591d868ed2 OP_EQUALVERIFY OP_CHECKSIG",
	                "hex" : "76a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac",
	                "reqSigs" : 1,
	                "type" : "pubkeyhash",
	                "addresses" : [
	                    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	                ]
	            },
	            "color" : 2
	        },
	        {
	            "value" : 6000000000,
	            "n" : 1,
	            "scriptPubKey" : {
	                "asm" : "OP_DUP OP_HASH160 8a6343b0603c3f5b16e812b27f833d591d868ed2 OP_EQUALVERIFY OP_CHECKSIG",
	                "hex" : "76a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac",
	                "reqSigs" : 1,
	                "type" : "pubkeyhash",
	                "addresses" : [
	                    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	                ]
	            },
	            "color" : 2
	        },
	        {
	            "value" : 9900000000,
	            "n" : 2,
	            "scriptPubKey" : {
	                "asm" : "OP_DUP OP_HASH160 8a6343b0603c3f5b16e812b27f833d591d868ed2 OP_EQUALVERIFY OP_CHECKSIG",
	                "hex" : "76a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac",
	                "reqSigs" : 1,
	                "type" : "pubkeyhash",
	                "addresses" : [
	                    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	                ]
	            },
	            "color" : 1
	        }
	    ],
	    "blockhash" : "000006bdab4a3ba1eff0ae8b433c0bf018f1c5bae076d01597984f981c3aa951",
	    "confirmations" : 11,
	    "time" : 1468474476,
	    "blocktime" : 1468474476
	}
`$ ./gcoin-cli getrawtransaction ff7ceb320c19a7808f1638d84578d2838bc15c4a98385332314090a652eeae21 1`

	{
	    "hex" : "01000000010000000000000000000000000000000000000000000000000000000000000000ffffffff6a473044022018bf2ba6731a685f70f97a9e541fc50adcb682da782647d52b9a33cfeac5761e022006bae3ed981fe8789275e1ff08aa91cc74f0787fe0a7ae59606223badcc1ac2e012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0bffffffff0100e40b54020000001976a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac020000000000000001000000",
	    "txid" : "ff7ceb320c19a7808f1638d84578d2838bc15c4a98385332314090a652eeae21",
	    "version" : 1,
	    "locktime" : 0,
	    "type" : "MINT",
	    "size" : 199,
	    "vin" : [
	        {
	            "coinbase" : "473044022018bf2ba6731a685f70f97a9e541fc50adcb682da782647d52b9a33cfeac5761e022006bae3ed981fe8789275e1ff08aa91cc74f0787fe0a7ae59606223badcc1ac2e012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b",
	            "scriptSig" : {
	                "asm" : "3044022018bf2ba6731a685f70f97a9e541fc50adcb682da782647d52b9a33cfeac5761e022006bae3ed981fe8789275e1ff08aa91cc74f0787fe0a7ae59606223badcc1ac2e01 02247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b",
	                "hex" : "473044022018bf2ba6731a685f70f97a9e541fc50adcb682da782647d52b9a33cfeac5761e022006bae3ed981fe8789275e1ff08aa91cc74f0787fe0a7ae59606223badcc1ac2e012102247c39fd5b694a8da4b22708de5190d183852ed470388b77613ec7be2e811c0b"
	            },
	            "sequence" : 4294967295
	        }
	    ],
	    "vout" : [
	        {
	            "value" : 10000000000,
	            "n" : 0,
	            "scriptPubKey" : {
	                "asm" : "OP_DUP OP_HASH160 8a6343b0603c3f5b16e812b27f833d591d868ed2 OP_EQUALVERIFY OP_CHECKSIG",
	                "hex" : "76a9148a6343b0603c3f5b16e812b27f833d591d868ed288ac",
	                "reqSigs" : 1,
	                "type" : "pubkeyhash",
	                "addresses" : [
	                    "1DcjAV7be3L4d7ss2grDRaPWi2P6GcZTjx"
	                ]
	            },
	            "color" : 2
	        }
	    ],
	    "blockhash" : "0000059954e98161f4b75e2a5b8ec09364485a6b7ec46d7b87b66f7ca632e16c",
	    "confirmations" : 22,
	    "time" : 1468474086,
	    "blocktime" : 1468474086
	}