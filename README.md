# TLS指纹数据库

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## 简介

TLS指纹数据库是一个包含大量TLS握手指纹的开源数据库项目。该数据库收集和整理了各种浏览器、应用程序和设备的TLS指纹信息，可用于网络安全分析、流量识别、异常检测等场景。

## 数据集特点

- 包含1000个TLS指纹文件
- 覆盖主流浏览器和应用程序
- 标准化JSON格式存储
- 持续更新和维护

## 数据结构

每个TLS指纹文件采用标准化的JSON格式，包含以下关键信息：
- TLS版本信息
- 加密套件列表
- 扩展字段
- 压缩方法
- 其他TLS握手参数

## 使用场景

- 网络安全分析
- 流量识别与分类
- 异常行为检测
- 渗透测试辅助
- 网络监控系统

## 安装与使用

### 克隆仓库

```bash
git clone https://github.com/123xiao/tls_fingerprint_db.git
cd tls_fingerprint_db/tls_json
```

## 数据示例
```bash
{
  "donate": "123xiao TLS指纹获取工具！ https://tls.123408.xyz",
  "ip": "47.147.7.73:33560",
  "http_version": "h2",
  "method": "GET",
  "user_agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/141.0.0.0 Safari/537.36",
  "tls": {
    "ciphers": [
      "TLS_GREASE (0xCACA)",
      "TLS_AES_128_GCM_SHA256",
      "TLS_AES_256_GCM_SHA384",
      "TLS_CHACHA20_POLY1305_SHA256",
      "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256",
      "TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256",
      "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384",
      "TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384",
      "TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256",
      "TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256",
      "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA",
      "TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA",
      "TLS_RSA_WITH_AES_128_GCM_SHA256",
      "TLS_RSA_WITH_AES_256_GCM_SHA384",
      "TLS_RSA_WITH_AES_128_CBC_SHA",
      "TLS_RSA_WITH_AES_256_CBC_SHA"
    ],
    "extensions": [
      {
        "name": "TLS_GREASE (0x2a2a)"
      },
      {
        "name": "server_name (0)",
        "server_name": "tls.123408.xyz"
      },
      {
        "name": "compress_certificate (27)",
        "algorithms": [
          "brotli (2)"
        ]
      },
      {
        "name": "extensionRenegotiationInfo (boringssl) (65281)",
        "data": "00"
      },
      {
        "name": "application_layer_protocol_negotiation (16)",
        "protocols": [
          "h2",
          "http/1.1"
        ]
      },
      {
        "name": "extended_master_secret (23)",
        "master_secret_data": "",
        "extended_master_secret_data": ""
      },
      {
        "name": "application_settings (17613)",
        "protocols": [
          "h2"
        ]
      },
      {
        "name": "signature_algorithms (13)",
        "signature_algorithms": [
          "ecdsa_secp256r1_sha256",
          "rsa_pss_rsae_sha256",
          "rsa_pkcs1_sha256",
          "ecdsa_secp384r1_sha384",
          "rsa_pss_rsae_sha384",
          "rsa_pkcs1_sha384",
          "rsa_pss_rsae_sha512",
          "rsa_pkcs1_sha512"
        ]
      },
      {
        "name": "psk_key_exchange_modes (45)",
        "PSK_Key_Exchange_Mode": "PSK with (EC)DHE key establishment (psk_dhe_ke) (1)"
      },
      {
        "name": "key_share (51)",
        "shared_keys": [
          {
            "TLS_GREASE (0x1a1a)": "00"
          },
          {
            "X25519MLKEM768 (4588)": "45c908deeb2bef300dc166b41c02c26f7a580541b53d66754f7c98db97787b1191f3b060f7cc4edf861f8178a087eb4363f55dff9b49ac31005473caa77463f9993b08d23be6e83f31568efac9b94cfc3011b1ce23633caad5087411046c397aca690daa2a2aca553659cc4a7a166b64ecb0e3aa9bf93831cad9cfe1bc409fa517059930705141fec383df959a9831b78f625fe900a5832b7d9da95e7c46bda57945710482863b6ad916b96957869d40096f517c3de45d8870551f1a206bf6bd8e100199924a60777fd9c7cd3b6649458b844cc01de2c228f5d65f7c9c0233acca17c6cf49681fdaec7c91711134e111e60802a4317148a43e2568a1274c1474a7c59763b00f763d36f02c00c3108a351c47484828f47359c2a868e7691e0ba9c64479e00aa753b1ab7d023a6ad9c16f35ac56598a9ce742ea51137bf3abdc63a320739597b5b65e50c29d92459b771f976c9f6060564b375007b29542903a1dabca890b64d110370369488e367a0656bbebb96829d2a32c7985187c2c5f5895dc0936889063abd2c4aa8012c7d025762342334b41689089e85235ae4c8f1621381a0b731c4373cfd0ab2c6311a2806bd1032c47f5280cd3b763c4315d5675c82392fc23b9e634be29239da0513e4191be17f58bdf33a0c1c4b58064962d736bf350aab05140b4fc819dbb9175672cfd408d65abb689eb6161c0c4c0e9a9cb46907ae5063ce2336872b02e1ab823f5ce9b5c5f7b087a849c38bb1014ecc756444293e55c7be4743f88313dfc24596a4248fef94db1f64a8f14163e2b766d4393cf0b51a970c3eac5c2ef7c87360b2ac2166c75a0c52f008eae62a3c1027d31a14627ea236756a471abb737092086d1b041cc997dab8365888bc925655cd48d49214063314807169dea300479c76075f138afb045ac8780f4b937a09c757fa19d9df5512fccce7865514ea36f8fb04735f5c28f258cae5b4fa5c655acb67fb7089e226ba246d00fd8b949526011ed403534cc1cb46274c5a81e5f5657309985fab28c8e6271cb644d70750014670f559a58cd631e2ba2c44c1b5bd5445d20b044746c7411406c3b70424fb3ab73c822389490ba51756e2c37062a5d0a22ba4143a1834bb340d9548ad6267383832dd166e3276e58ec7e866a3d4b029c94349ca2d999e7e0428c04aac294334a1a901afbb207b49f5a898efde39be1a697b47752300791a47b83ba3451588b10191b9d7f7498f3b371d2c2cf764baea9832efffca396b1b9a2aa3231e5bc9c7351b7ccafb4c67dd8b50bf5566aadf87e99e74a5c2c56ed5c95a6daba0ad7756ce4039cc5568f58bf0611cd4c88298c1b5174d91ea8c7ac9eb283d5d68d7ef65c8cb8a88866bc8c423af645682108288a2443a665b2e3a65c71f9850ba6716ddb82c912aff4e3c77181a74c1752a3029ac815a57f9c033e319b9955483d26a402a916b65ba5a35ca6f58222621a2321704ff29123fdd5656f50bec8a66c11cbcc4afc4cac3c8f20d30228d03c8ee0966709ce4c4ab3f44b8f41e54338e4b74d5391f61a6975066ff2b244c3f455fa435d32c03266d870e945bf9769a5d2774643c8c2d225ca4b17110660bb9198c9be4a44b049ac32d08494943c84480fb56070bce1f27ab2edfd6358f3ab5d65971292c7f9875750c251d363595b8179832463ed2c77149f5cc52e45130e52aa45291bf4069040"
          },
          {
            "X25519 (29)": "5fbd6142128834a4fdc72a2e203b58e8f4351c671e6ed677371258e37006aa72"
          }
        ]
      },
      {
        "name": "status_request (5)",
        "status_request": {
          "certificate_status_type": "OSCP (1)",
          "responder_id_list_length": 0,
          "request_extensions_length": 0
        }
      },
      {
        "name": "session_ticket (35)",
        "data": ""
      },
      {
        "name": "supported_groups (10)",
        "supported_groups": [
          "TLS_GREASE (0x1a1a)",
          "X25519MLKEM768 (4588)",
          "X25519 (29)",
          "P-256 (23)",
          "P-384 (24)"
        ]
      },
      {
        "name": "ec_point_formats (11)",
        "elliptic_curves_point_formats": [
          "0x00"
        ]
      },
      {
        "name": "signed_certificate_timestamp (18)"
      },
      {
        "name": "supported_versions (43)",
        "versions": [
          "TLS_GREASE (0xcaca)",
          "TLS 1.3",
          "TLS 1.2"
        ]
      },
      {
        "name": "extensionEncryptedClientHello (boringssl) (65037)",
        "data": "0000010001ba0020c93ab093a418ff1b7b1d76e2900db419b8fb1a7ad16e0042560e72eb142d981f00d04f0b74cdf37cc0601b042022572375ae8f82c9b9e9efcf23ebccf83c934242da4328f18e54442610b60c10f07ea9f17f8e0671a10d200576c233866e4ff49994637c0fe4bd248ea47757aee8688fa7fa29fa29e63578ffb89c23b64240fc1c6d674bd3525d9d2745b305668d0a4134fa130bf4a5a88c9d106b6bce6409334124114c07bb49bad765f9e59a11f67f0aedf882190cc7f9a6e725bd8c6bc62465ae4a4170ab0183e0dc89868c2208e708a7872f0ea775fa790b4c336224e57f3aa6c838fde4c5d0f3b313c7f62b5af3ee5d"
      },
      {
        "name": "TLS_GREASE (0x3a3a)"
      }
    ],
    "tls_version_record": "771",
    "tls_version_negotiated": "772",
    "ja3": "771,4865-4866-4867-49195-49199-49196-49200-52393-52392-49171-49172-156-157-47-53,0-27-65281-16-23-17613-13-45-51-5-35-10-11-18-43-65037,4588-29-23-24,0",
    "ja3_hash": "0a9e529cd9052e33524e81e0c8e8d9bf",
    "ja4": "t13d1516h2_8daaf6152771_d8a2da3f94cd",
    "ja4_r": "t13d1516h2_002f,0035,009c,009d,1301,1302,1303,c013,c014,c02b,c02c,c02f,c030,cca8,cca9_0005,000a,000b,000d,0012,0017,001b,0023,002b,002d,0033,44cd,fe0d,ff01_0403,0804,0401,0503,0805,0501,0806,0601",
    "peetprint": "GREASE-772-771|2-1.1|GREASE-4588-29-23-24|1027-2052-1025-1283-2053-1281-2054-1537|1|2|GREASE-4865-4866-4867-49195-49199-49196-49200-52393-52392-49171-49172-156-157-47-53|0-10-11-13-16-17613-18-23-27-35-43-45-5-51-65037-65281-GREASE-GREASE",
    "peetprint_hash": "1d4ffe9b0e34acac0bd883fa7f79d7b5",
    "client_random": "d23ef4dc9aac03dccfddad7255cfbcb364a96a1824160ebf5f92401d9d7afe8f",
    "session_id": "bf4c8d486198e2b67eaa1c692266a7b810e5728b35fd0aae165e541fe921a0d2"
  },
  "http2": {
    "akamai_fingerprint": "1:65536;2:0;4:6291456;6:262144|15663105|0|m,a,s,p",
    "akamai_fingerprint_hash": "52d84b11737d980aef856699f885ca86",
    "sent_frames": [
      {
        "frame_type": "SETTINGS",
        "length": 24,
        "settings": [
          "HEADER_TABLE_SIZE = 65536",
          "ENABLE_PUSH = 0",
          "INITIAL_WINDOW_SIZE = 6291456",
          "MAX_HEADER_LIST_SIZE = 262144"
        ]
      },
      {
        "frame_type": "WINDOW_UPDATE",
        "length": 4,
        "increment": 15663105
      },
      {
        "frame_type": "HEADERS",
        "stream_id": 1,
        "length": 367,
        "headers": [
          ":method: GET",
          ":authority: tls.123408.xyz",
          ":scheme: https",
          ":path: /api/ip",
          "sec-ch-ua-platform: \\\"Windows\\",
          "user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/141.0.0.0 Safari/537.36",
          "sec-ch-ua: \\\"Google Chrome\\\";v=\\\"141\\\", \\\"Not?A_Brand\\\";v=\\\"8\\\", \\\"Chromium\\\";v=\\\"141\\",
          "sec-ch-ua-mobile: ?0",
          "accept: */*",
          "origin: https://ip.123408.xyz",
          "sec-fetch-site: same-site",
          "sec-fetch-mode: cors",
          "sec-fetch-dest: empty",
          "referer: https://ip.123408.xyz/",
          "accept-encoding: gzip, deflate, br, zstd",
          "accept-language: zh-CN,zh;q=0.9",
          "priority: u=1, i"
        ],
        "flags": [
          "EndStream (0x1)",
          "EndHeaders (0x4)",
          "Priority (0x20)"
        ],
        "priority": {
          "weight": 220,
          "depends_on": 0,
          "exclusive": 1
        }
      }
    ]
  },
  "tcpip": {
    "cap_length": 158,
    "dst_port": 443,
    "src_port": 33560,
    "ip": {
      "id": 10593,
      "tos": 40,
      "ttl": 48,
      "ip_version": 4,
      "dst_ip": "172.18.0.2",
      "src_ip": "47.147.7.73"
    },
    "tcp": {
      "ack": 1120209685,
      "checksum": 13046,
      "seq": 4220111694,
      "window": 515
    }
  }
}
```


## 贡献指南

欢迎提交新的TLS指纹数据或改进现有数据：
1. Fork本仓库
2. 添加或修改指纹数据
3. 提交Pull Request

## 许可证

本项目采用MIT许可证，详情请参见[LICENSE](LICENSE)文件。

## 免责声明

本数据库仅供安全研究和合法用途，使用者需遵守相关法律法规。