# DefiHack Examples

project(twitter) | date | value | analysis | transaction | poc | notes

---

[Access Control](#access-control)

[Arbitrary External Call Vulnerability](#arbitrary-external-call-vulnerability)

[Business logic flaw](#business-logic-flaw)

[Input Validation](#input-validation)

[Price Manipulation](#price-manipulation)

[Reentrancy](#reentrancy)

[Reflection token](#reflection-token)

---
### Access Control

* **[LeetSwap](https://twitter.com/LeetSwap)** | 20230801 | $630K | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1686217464051539968), [peckshield](https://twitter.com/peckshield/status/1686209024587710464)] | [Transaction](https://basescan.org/tx/0xbb837d417b76dd237b4418e1695a50941a69259a1c4dee561ea57d982b9f10ec) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Leetswap_exp.sol) | _

* **[ARA](https://twitter.com/AraBlocks)** | 20230618 | $125K | [[BeosinAlert](https://twitter.com/BeosinAlert/status/1670638160550965248), [Phalcon_xyz](https://twitter.com/Phalcon_xyz/status/1670700964272295936)] | [Transaction](https://bscscan.com/tx/0xd87cdecd5320301bf9a985cc17f6944e7e7c1fbb471c80076ef2d031cc3023b2) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ARA_exp.sol) | _

* **DEPUSDT_LEVUSDC** | 20230615 | $105k | [[numencyber](https://twitter.com/numencyber/status/1669278694744150016?cxt=HHwWgMDS9Z2IvKouAAAA), [Phalcon_xyz](https://twitter.com/Phalcon_xyz/status/1669290094585577474), [BeosinAlert](https://twitter.com/BeosinAlert/status/1669288074784718849)] | [[Tx1](https://etherscan.io/tx/0xf0a13b445674094c455de9e947a25bade75cac9f5176695fca418898ea25742f) , [Tx2](https://etherscan.io/tx/0x800a5b3178f680feebb81af69bd3dff791b886d4ce31615e601f2bb1f543bb2e)] | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/DEPUSDT_LEVUSDC_exp.sol) | _

* **[Local Trade LCT](https://twitter.com/LOCALTRADERSCL)** | 20230524 | $~384 BNB | [[numencyber](https://twitter.com/numencyber/status/1661213691893944320)] | [[Tx1](https://bscscan.com/tx/0x57b589f631f8ff20e2a89a649c4ec2e35be72eaecf155fdfde981c0fec2be5ba), [Tx2](https://bscscan.com/tx/0xbea605b238c85aabe5edc636219155d8c4879d6b05c48091cf1f7286bd4702ba), [Tx3](https://bscscan.com/tx/0x49a3038622bf6dc3672b1b7366382a2c513d713e06cb7c91ebb8e256ee300dfb), [Tx4](https://bscscan.com/tx/0x042b8dc879fa193acc79f55a02c08f276eaf1c4f7c66a33811fce2a4507cea63)] | [[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/LocalTrader_exp.sol), [POC2](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/LocalTrader2_exp.sol) | _

* **landNFT** | 20230514 | $149.6K | [[BeosinAlert](https://twitter.com/BeosinAlert/status/1658000784943124480)] | [Transaction](https://bscscan.com/tx/0xe4db1550e3aa78a05e93bfd8fbe21b6eba5cce50dc06688949ab479ebed18048) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/landNFT_exp.sol) | nft mint

* **[Melo](https://twitter.com/melotoken)** | 20230506 | $90K | [[peckshield](https://twitter.com/peckshield/status/1654667621139349505)] | [Transaction](https://bscscan.com/tx/0x3f1973fe56de5ecd59a815d3b14741cf48385903b0ccfe248f7f10c2765061f7) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Melo_exp.sol) | public mint

* **[LaunchZone](https://twitter.com/launchzoneann)** | 20230227 | ~$320,000 | [[Immunefi](https://twitter.com/immunefi/status/1630210901360951296), [LaunchZone](https://twitter.com/launchzoneann/status/1631538253424918528)] | [Transaction](https://bscscan.com/tx/0xaee8ef10ac816834cd7026ec34f35bdde568191fe2fa67724fcf2739e48c3cae) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/LaunchZone_exp.sol) | _

* **[swapX](https://twitter.com/SwapXOfficial)** | 20230227 | ~$1M | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1630111965942018049), [peckshield](https://twitter.com/peckshield/status/1630100506319413250), [CertiKAlert](https://twitter.com/CertiKAlert/status/1630241903839985666)] | [Transaction](https://bscscan.com/tx/0x3ee23c1585474eaa4f976313cafbc09461abb781d263547c8397788c68a00160) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SwapX_exp.sol) | _

* **[ULME](https://twitter.com/)** | 20221026 | ~$200k (resulted in ~$50k profit) | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1584839309781135361), [BeosinAlert](https://twitter.com/BeosinAlert/status/1584888021299916801)] | [Transaction](https://bscscan.com/tx/0xdb9a13bc970b97824e082782e838bdff0b76b30d268f1d66aac507f1d43ff4ed) | [POC](src/test/ULME.sol) | _

* **[HPAY](https://twitter.com/)** | 20221018 | 115 BNB | [[Supremacy_CA](https://twitter.com/Supremacy_CA/status/1582345448190140417)] | [Transaction](https://bscscan.com/tx/0x62e959fe88128cc592b2061339e887e30b3160534a1171abad143da82900dd25) | [POC](src/test/HPAY_exp.sol) | _

* **[Uerii Token](https://twitter.com/Uerii_Official)** | 20221017 | $2.4k | [[PeckShield](https://twitter.com/peckshield/status/1581988895142526976)] | [Transaction](https://etherscan.io/tx/0xf4a3d0e01bbca6c114954d4a49503fc94dfdbc864bded5530b51a207640d86b5) | [POC](src/test/Uerii_exp.sol) | _

* **[Templedao](https://twitter.com/templedao)** | 20221011 | $2.3 million | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1579843881893769222)] | [Transaction](https://etherscan.io/tx/0x8c3f442fc6d640a6ff3ea0b12be64f1d4609ea94edd2966f42c01cd9bdcf04b5) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Templedao_exp.sol) | _

* **[Ragnarok Online Invasion](https://twitter.com/)** | 20220908 | $44,000 | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1567746825616236544), [CertiKAlert](https://twitter.com/CertiKAlert/status/1567754904663429123)] | [Transaction](https://bscscan.com/tx/0x0e14cb7eabeeb2a819c52f313c986a877c1fa19824e899d1b91875c11ba053b0) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ROI_exp.sol) | _
* **[FlippazOne NFT](https://opensea.io/zh-CN/collection/flippazone)** | 20220706 | ownerWithdrawAll | [[bertcmiller](https://twitter.com/bertcmiller/status/1544496577338826752)] | [Transaction](https://etherscan.io/tx/0x8bded20c1db5a1d5f595b15e682a95ce11d3c895d6031147fa49c4ffa5729a30) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/FlippazOne.sol) | _

* **[GYMNetwork](https://twitter.com/GymNet_Official)** | 20220608 | $2.1 million | [[peckshield](https://twitter.com/peckshield/status/1534423219607719936), [1nf0s3cpt](https://twitter.com/1nf0s3cpt/status/1534464698069884929), [jinse](https://www.jinse.com/news/blockchain/1658455.html)] | [Transaction](https://bscscan.com/tx/0x8432c1c6613995eeea8a3ae2cfeb9577913db6b7b35dbe26a8c56c02066096e6) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Gym_2_exp.sol) | _

* **[Sandbox LAND](https://twitter.com/TheSandboxGame)** | 20220208 | - | [[SlowMist](https://slowmist.medium.com/the-vulnerability-behind-the-sandbox-land-migration-2abf68933170)] | [[Transaction](https://etherscan.io/tx/0x34516ee081c221d8576939f68aee71e002dd5557180d45194209d6692241f7b1)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Sandbox_exp.sol) | _

* **[DAO Maker](https://twitter.com/daomaker)** | 20210903 | $4M | [[Twitter](https://twitter.com/Mudit__Gupta/status/1434059922774237185)] | [[Transaction](https://etherscan.io/tx/0xd5e2edd6089dcf5dca78c0ccbdf659acedab173a8ab3cb65720e35b640c0af7c)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/DaoMaker_exp.sol) | _

* **[88mph](https://twitter.com/88mphapp)** | 20210607 | $6.5M | [[Medium](https://medium.com/immunefi/88mph-function-initialization-bug-fix-postmortem-c3a2282894d3)] | [[Address](https://etherscan.io/address/0xf0b7de03134857391d8d43ed48e20edf21461097)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/88mph_exp.sol) | _


### Arbitrary External Call Vulnerability

* **[MIMSpell](https://twitter.com/MIM_Spell)** | 20230620 | ~$17k | [[hexagate_](https://twitter.com/hexagate_/status/1671188024607100928?cxt=HHwWgMC--e2poLEuAAAA)] | [Transaction](https://etherscan.io/tx/0x2c9f87e285026601a2c8903cf5f10e5b3655fbd0264490c41514ce073c42a9c3) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/MIMSpell_exp.sol) | _

* **[RevertFinance](https://twitter.com/revertfinance)** | 20230218 | ~$30k | [[Mirror.xyz](https://mirror.xyz/revertfinance.eth/3sdpQ3v9vEKiOjaHXUi3TdEfhleAXXlAEWeODrRHJtU)] | [Transaction](https://etherscan.io/tx/0xdaccbc437cb07427394704fbcc8366589ffccf974ec6524f3483844b043f31d5) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/RevertFinance_exp.sol) | _

* **[Dexible](https://twitter.com/DexibleApp)** | 20230217 | ~$1.5M | [[peckshield](https://twitter.com/peckshield/status/1626493024879673344), [MevRefund](https://twitter.com/MevRefund/status/1626450002254958592)] | [Transaction](https://etherscan.io/tx/0x138daa4cbeaa3db42eefcec26e234fc2c89a4aa17d6b1870fc460b2856fd11a6) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Dexible_exp.sol) | _

* **[CowSwap](https://twitter.com/CoWSwap)** | 20230207 | ~$120k | [[MevRefund](https://twitter.com/MevRefund/status/1622793836291407873), [peckshield](https://twitter.com/peckshield/status/1622801412727148544)] | [Transaction](https://etherscan.io/tx/0x90b468608fbcc7faef46502b198471311baca3baab49242a4a85b73d4924379b) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/CowSwap_exp.sol) | _

* **[Rubic](https://twitter.com/CryptoRubic)** | 20221225 | $1.5M | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1606993118901198849), [peckshield](https://twitter.com/peckshield/status/1606937055761952770)] | [Transaction](https://etherscan.io/tx/0x9a97d85642f956ad7a6b852cf7bed6f9669e2c2815f3279855acf7f1328e7d46) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Rubic_exp.sol) | _

* **[MulticallWithoutCheck](https://twitter.com/)** | 20221024 | $600 |  | [Transaction](https://polygonscan.com/tx/0xd1c216619b829fb5a255833a977dce982c8b5183fbe3baa9da710ef4c37a8bb8) | [POC](src/test/MulticallWithoutCheck_exp.sol) | _

* **[BrahTOPG](https://etherscan.io/tx/0xeaef2831d4d6bca04e4e9035613be637ae3b0034977673c1c2f10903926f29c0)** | 20221109 | $89k | [SlowMist_Team](https://twitter.com/SlowMist_Team/status/1590685173477101570) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BrahTOPG_exp.sol) | _

* **[Rabby_io](https://twitter.com/Rabby_io)** | 20221011 | ~200,000 US$ | [[Supremacy_CA](https://twitter.com/Supremacy_CA/status/1579813933669486592), [SlowMist_Team](https://twitter.com/SlowMist_Team/status/1579839744128978945), [BeosinAlert](https://twitter.com/BeosinAlert/status/1579856733178331139)] | [Transaction](https://etherscan.io/tx/0xce0935010baf445e300d4d600caac7fc1fecb5ccb092cdbef57904aa7e5408b2) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/RabbyWallet_SwapRouter.exp.sol) | _

* **[MEV_0ad8](https://twitter.com/renprotocol)** | 20221108 | $282k | [Supremacy_CA](https://twitter.com/Supremacy_CA/status/1590337718755954690) | [Transaction](https://etherscan.io/tx/0x674f74b30a3d7bdf15fa60a7c29d96a402ea894a055f624164a8009df98386a0) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/MEV_0ad8.t.sol) | _

### Business Logic Flaw

* **[ShidoGlobal](https://twitter.com/ShidoGlobal)** | 20230623 | $997BNB | [[Phalcon_xyz](https://twitter.com/Phalcon_xyz/status/1672473343734480896), [AnciliaInc](https://twitter.com/AnciliaInc/status/1672382613473083393)] | [Transaction](https://bscscan.com/tx/0x72f8dd2bcfe2c9fbf0d933678170417802ac8a0d8995ff9a56bfbabe3aa712d6) | [[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SHIDO_exp.sol), [POC2](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ShidoGlobal_exp.sol)] | _different-price-between-two-pools_

* **[LFI Token](https://twitter.com/LunaFi_Project)** | 20230523 | $36K | [[AnciliaInc](https://twitter.com/AnciliaInc/status/1660767088699666433)] | [Transaction](https://polygonscan.com/tx/0xdd82fde0cc2fb7bdc078aead655f6d5e75a267a47c33fa92b658e3573b93ef0c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/LFI_exp.sol) | _

* **[Bitpaidio](https://twitter.com/bitpaidio)** | 20230513 | $30K | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1657715018908180480)] | [Transaction](https://bscscan.com/tx/0xace112925935335d0d7460a2470a612494f910467e263c7ff477221deee90a2c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Bitpaidio_exp.sol) | _

* **[SellToken](https://twitter.com/TrustTheTrident)** | 20230511 | $95k | [[AnciliaInc](https://twitter.com/AnciliaInc/status/1656337400329834496), [AnciliaInc2](https://twitter.com/AnciliaInc/status/1656341587054702598)] | [Transaction](https://bscscan.com/tx/0xace112925935335d0d7460a2470a612494f910467e263c7ff477221deee90a2c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SELLC_exp.sol) | _

* **[SNK]()** | 20230510 | $197k | [[Phalcon_xyz](https://twitter.com/Phalcon_xyz/status/1656176776425644032)] | [Transaction](https://bscscan.com/tx/0xace112925935335d0d7460a2470a612494f910467e263c7ff477221deee90a2c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SNK_exp.sol) | _

* **[Axioma](https://twitter.com/AxiomaHolding)** | 20230424 | $21BNB | [[HypernativeLabs](https://twitter.com/HypernativeLabs/status/1650382589847302145)] | [Transaction](https://bscscan.com/tx/0x05eabbb665a5b99490510d0b3f93565f394914294ab4d609895e525b43ff16f2) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Axioma_exp.sol) | _

* **[DBW](https://twitter.com/BigwinnerDBW)** | 20230325 | $24k | [[BeosinAlert](https://twitter.com/BeosinAlert/status/1639655134232969216), [AnciliaInc](https://twitter.com/AnciliaInc/status/1639289686937210880)] | [Transaction](https://bscscan.com/tx/0x3b472f87431a52082bae7d8524b4e0af3cf930a105646259e1249f2218525607) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/DBW_exp.sol) | _

* **[EulerFinance](https://twitter.com/eulerfinance)** | 20230313 | ~$200M | [[Frank Researcher](https://twitter.com/FrankResearcher/status/1635241475989721089), [nomorebear](https://twitter.com/nomorebear/status/1635230621856600064), [PeckShield](https://twitter.com/peckshield/status/1635229594596036608), [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1635262150624305153)] | [Transaction](https://etherscan.io/tx/0xc310a0affe2169d1f6feec1c63dbc7f7c62a887fa48795d327d4d2da2d6b111d) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Euler_exp.sol) | _

* **[DYNA](https://twitter.com/fi_dynamic)** | 20230222 | ~$21k | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1628319536117153794), [BeosinAlert](https://twitter.com/BeosinAlert/status/1628301635834486784)] | [Transaction 1](https://bscscan.com/tx/0x06bbe093d9b84783b8ca92abab5eb8590cb2321285660f9b2a529d665d3f18e4), [Transaction 2](https://bscscan.com/tx/0xc09678fec49c643a30fc8e4dec36d0507dae7e9123c270e1f073d335deab6cf0) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/DYNA_exp.sol) | _

* **[Starlink](https://twitter.com/StarLinkETH)** | 20230217 | ~$12k | [[NumenAlert](https://twitter.com/NumenAlert/status/1626447469361102850), [bbbb](https://twitter.com/bbbb/status/1626392605264351235)] | [Transaction](https://bscscan.com/tx/0x146586f05a4513136deab3557ad15df8f77ffbcdbd0dd0724bc66dbeab98a962) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Starlink_exp.sol) | _

* **[Platypusdefi](https://twitter.com/Platypusdefi)** | 20230217 | ~$8.5M | [[peckshield](https://twitter.com/peckshield/status/1626367531480125440), [spreekaway](https://twitter.com/spreekaway/status/1626319585040338953)] | [Transaction](https://snowtrace.io/tx/0x1266a937c2ccd970e5d7929021eed3ec593a95c68a99b4920c2efa226679b430) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Platypus_exp.sol) | _

* **QTNToken** | 20230118 | ~2ETH | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1615625901739511809)] | [Transaction 1](https://etherscan.io/tx/0x37cb8626e45f0749296ef080acb218e5ccc7efb2ae4d39c952566dc378ca1c4c), [Transaction 2](https://etherscan.io/tx/0xfde10ad92566f369b23ed5135289630b7a6453887c77088794552c2a3d1ce8b7) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/QTN_exp.sol) | _

* **[ThoreumFinance](https://twitter.com/ThoreumFinance)** | 20230119 | ~2000 BNB | [[AnciliaInc](https://twitter.com/AnciliaInc/status/1615944396134043648)] | [Transaction](https://bscscan.com/tx/0x3fe3a1883f0ae263a260f7d3e9b462468f4f83c2c88bb89d1dee5d7d24262b51) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ThoreumFinance_exp.sol) | _

* **[UPSToken](https://twitter.com/UpswingFinance)** | 20230118 | ~22 ETH | [[QuillAudits](https://twitter.com/QuillAudits/status/1615634917802807297)] | [Transaction](https://etherscan.io/tx/0x4b3df6e9c68ae482c71a02832f7f599ff58ff877ec05fed0abd95b31d2d7d912) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Upswing_exp.sol) | _

* **BRA** | 20230110 | 819 BNB (~224k$) | [[CertiKAlert](https://twitter.com/CertiKAlert/status/1612674916070858753), [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1612701106982862849)] | [Transaction 1](https://bscscan.com/tx/0x6759db55a4edec4f6bedb5691fc42cf024be3a1a534ddcc7edd471ef205d4047), [Transaction 2](https://bscscan.com/tx/0x4e5b2efa90c62f2b62925ebd7c10c953dc73c710ef06695eac3f36fe0f6b9348) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BRA.exp.sol) | _

* **[GDS](https://twitter.com/GDS_chain)** | 20230103 | $180k | [[peckshield](https://twitter.com/peckshield/status/1610095490368180224), [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1610167174978760704)] | [Transaction 1](https://bscscan.com/tx/0xf9b6cc083f6e0e41ce5e5dd65b294abf577ef47c7056d86315e5e53aa662251e), [Transaction 2](https://bscscan.com/tx/0x2bb704e0d158594f7373ec6e53dc9da6c6639f269207da8dab883fc3b5bf6694) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/GDS_exp.sol) | Business Logic Flaw

* **[ElasticSwap](https://twitter.com/ElasticSwap)** | 20221213 | $845k | [QuillAudits](https://quillaudits.medium.com/decoding-elastic-swaps-850k-exploit-quillaudits-9ceb7fcd8d1a) | [Transaction](https://etherscan.io/tx/0xb36486f032a450782d5d2fac118ea90a6d3b08cac3409d949c59b43bcd6dbb8f) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ElasticSwap_exp.sol) | Business Logic Flaw

* **[SEAMAN](#)** | 20221129 | $7k | [PeckShield](https://twitter.com/peckshield/status/1597493955939405825) | [Transaction](https://bscscan.com/tx/0x6f1af27d08b10caa7e96ec3d580bf39e29fd5ece00abda7d8955715403bf34a8) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SEAMAN_exp.sol) | Business Logic Flaw

* **[sDAO](https://twitter.com/SportsDao1)** | 20221121 | $13k | [8olidity](https://twitter.com/8olidity/status/1594693686398316544) | [Transaction](https://bscscan.com/tx/0xb3ac111d294ea9dedfd99349304a9606df0b572d05da8cedf47ba169d10791ed) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SDAO_exp.sol) | Business Logic Flaw

* **[BDEX](https://twitter.com/)** | 20221105 | 16WBNB | [[BeosinAlert](https://twitter.com/BeosinAlert/status/1588579143830343683)] | [Transaction](https://bscscan.com/tx/0xe7b7c974e51d8bca3617f927f86bf907a25991fe654f457991cbf656b190fe94) | [POC](src/test/BDEX_exp.sol) | _

* **[Bad Guys by RPF](https://opensea.io/collection/badguysbyrpf)** | 20220902 | 400 NFTs | [[RugDoctorApe](https://twitter.com/RugDoctorApe/status/1565739119606890498)] | [Transaction](https://etherscan.io/tx/0x27e64a8215ae1528245c912bcca09883fdd7cce69249bd5d5d1c0eecf5297b96) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BadGuysbyRPF_exp.sol) | _Missing Check For Number of NFT to Mint_

### Input Validation

* **[BabyDogeCoin](https://twitter.com/TrustTheTrident)** | 20230529 | ~135k | [[Phalcon_xyz](https://twitter.com/Phalcon_xyz/status/1662744426475831298)] | [[Transaction](https://bscscan.com/tx/0x098e7394a1733320e0887f0de22b18f5c71ee18d48a0f6d30c76890fb5c85375)] | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BabyDogeCoin_exp.sol) | _

* **[SellToken](https://twitter.com/TrustTheTrident)** | 20230514 | ~unknow | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1657715018908180480)] | [[Transaction](https://bscscan.com/tx/0xfe80df5d689137810df01e83b4bb51409f13c865e37b23059ecc6b3d32347136), [Transaction2](https://bscscan.com/tx/0x8a453c61f0024e8e11860729083088507a02a38100da8b0c3b2d558788662fa0)] | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SELLC02_exp.sol) | _

* **[SushiSwap](https://twitter.com/SushiSwap)** | 20230409 | >$3.3M | [[peckshield](https://twitter.com/peckshield/status/1644907207530774530), [SlowMist_Team](https://twitter.com/SlowMist_Team/status/1644936375924584449), [AnciliaInc](https://twitter.com/AnciliaInc/status/1644925421006520320)] | [Transaction](https://etherscan.io/tx/0xea3480f1f1d1f0b32283f8f282ce16403fe22ede35c0b71a732193e56c5c45e8) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Sushi_Router_exp.sol) | _V3Callback_

* **[OmniEstate](https://twitter.com/omniestategroup)** | 20230117 | $70k(236 BNB) | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1615232012834705408)] | [Transaction 1](https://bscscan.com/tx/0x49bed801b9a9432728b1939951acaa8f2e874453d39c7d881a62c2c157aa7613), [Transaction 2](https://bscscan.com/tx/0xa916674fb8203fac6d78f5f9afc604be468a514aa61ea36c6d6ef26ecfbd0e97) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/OmniEstate_exp.sol) | _

* **[Phoenix](https://twitter.com/Phoenix__PHX)** | 20230307 | ~$100k | [[HypernativeLabs](https://twitter.com/HypernativeLabs/status/1633090456157401088)] | [Transaction](https://polygonscan.com/tx/0x6fa6374d43df083679cdab97149af8207cda2471620a06d3f28b115136b8e2c4) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Phoenix_exp.sol) | _fake-token_

* **[SheepFarm](https://twitter.com/Sheep_Farm22)** | 20221116 | ~1BNB | [AnciliaInc](https://twitter.com/AnciliaInc/status/1592658104394473472) | [Transaction](https://bscscan.com/tx/0x5735026e5de6d1968ab5baef0cc436cc0a3f4de4ab735335c5b1bd31fa60c582) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SheepFarm_exp.sol) | _

* **[OlympusDAO](https://twitter.com/OlympusDAO)** | 20221021 | ~$292K (30500 OHM) | [[PeckShield](https://twitter.com/peckshield/status/1583416829237526528)] | [Transaction](https://etherscan.io/tx/0x3ed75df83d907412af874b7998d911fdf990704da87c2b1a8cf95ca5d21504cf) | [POC](src/test/OlympusDao.exp.sol) | _

* **[BabySwap](https://twitter.com/babyswap_bsc)** | 20221001 | - | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1576441612812836865)] | [Transaction](https://bscscan.com/tx/0xcca7ea9d48e00e7e32e5d005b57ec3cac28bc3ad0181e4ca208832e62aa52efe) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BabySwap_exp.sol) | _fake-router_

### Price Manipulation

* **[Themis](https://twitter.com/ThemisProtocol)** | 20230628 | $370k | [[BeosinAlert](https://twitter.com/BeosinAlert/status/1673930979348717570), [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1673897088617426946)] | [Transaction](https://arbiscan.io/tx/0xff368294ccb3cd6e7e263526b5c820b22dea2b2fd8617119ba5c3ab8417403d8) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Themis_exp.sol) | _

* **[CFC](https://twitter.com/safeanwang)** | 20230615 | $16k | [[Phalcon_xyz](https://twitter.com/Phalcon_xyz/status/1669556040445362176), [hexagate_](https://twitter.com/hexagate_/status/1669280632738906113), [HypernativeLabs](https://twitter.com/HypernativeLabs/status/1669243919450636289)] | [Transaction](https://explorer.phalcon.xyz/tx/bsc/0xa3c130ed8348919f73cbefce0f22d46fa381c8def93654e391ddc95553240c1e) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/CFC_exp.sol) | _skim_

* **[UN]()** | 20230606 | $26k | [[MetaTrustAlert](https://twitter.com/MetaTrustAlert/status/1667041877428932608)] | [Transaction](https://bscscan.com/tx/0xff5515268d53df41d407036f547b206e288b226989da496fda367bfeb31c5b8b) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/UN_exp.sol) | _skim_

* **[ERC20TokenBank]()** | 20230531 | $111K | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1663810037788311561)] | [Transaction](https://etherscan.io/tx/0x578a195e05f04b19fd8af6358dc6407aa1add87c3167f053beb990d6b4735f26) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ERC20TokenBank_exp.sol) | _

* **[Jimbo](https://twitter.com/jimbosprotocol)** | 20230529 | $8M | [[cryptofishx](https://twitter.com/cryptofishx/status/1662888991446941697), [yicunhui2](https://twitter.com/yicunhui2/status/1663793958781353985)] | [[Tx](https://arbiscan.io/tx/0xf9baf8cee8973cf9700ae1b1f41c625d7a2abdbcbc222582d24a8f2f790d0b5a), [Tx2](https://arbiscan.io/tx/0xfda5464e97043a2d0093cbed6d0a64f6a86049f5e9608c014396a7390188670e), [Tx3](https://arbiscan.io/tx/0x3c6e053faecd331883641c1d23c9d9d37d065e4f9c4086e94a3c34bf8702618a), [Tx4](https://arbiscan.io/tx/0x44a0f5650a038ab522087c02f734b80e6c748afb207995e757ed67ca037a5eda)] | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Jimbo_exp.sol) | Protocol-specific price manipulation

* **[LW]()** | 20230512 | $50K | [[PeckShieldAlert](https://twitter.com/PeckShieldAlert/status/1656850634312925184), [hexagate_](https://twitter.com/hexagate_/status/1657051084131639296)] | [Transaction](https://bscscan.com/tx/0xb846f3aeb9b3027fe138b23bbf41901c155bd6d4b24f08d6b83bd37a975e4e4a) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/LW_exp.sol) | FlashLoan

* **[Allbridge](https://twitter.com/Allbridge_io)** | 20230402 | $550k | [[peckshield](https://twitter.com/peckshield/status/1642356701100916736), [BeosinAlert](https://twitter.com/BeosinAlert/status/1642372700726505473)] | [Transaction](https://bscscan.com/tx/0x7ff1364c3b3b296b411965339ed956da5d17058f3164425ce800d64f1aef8210) | [POC1](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Allbridge_exp.sol), [POC2](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Allbridge_exp2.sol) | _

* **[DKP]()** | 20230308 | ~$80K | [[CertiKAlert](https://twitter.com/CertiKAlert/status/1633421908996763648)] | [Transaction 1](https://bscscan.com/tx/0x0c850f54c1b497c077109b3d2ef13c042bb70f7f697201bcf2a4d0cb95e74271), [Transaction 2](https://bscscan.com/tx/0x2d31e45dce58572a99c51357164dc5283ff0c02d609250df1e6f4248bd62ee01) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/DKP_exp.sol) | _

* **[RoeFinance](https://twitter.com/RoeFinance)** | 20230112 | $80k | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1613267000913960976)] | [Transaction](https://etherscan.io/tx/0x927b784148b60d5233e57287671cdf67d38e3e69e5b6d0ecacc7c1aeaa98985b) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/RoeFinance_exp.sol) | _

* **[Nmbplatform](https://twitter.com/nmbplatform)** | 20221214 | $76k | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1602877048124735489)] | [Transaction](https://bscscan.com/tx/0x7d2d8d2cda2d81529e0e0af90c4bfb39b6e74fa363c60b031d719dd9d153b012) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Nmbplatform_exp.sol) | _

* **[BGLD (Deflationary token)]()** | 20221212 | $18k | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1602335214356660225)] | [Transaction](https://bscscan.com/tx/0xea108fe94bfc9a71bb3e4dee4a1b0fd47572e6ad6aba8b2155ac44861be628ae) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BGLD_exp.sol) | _

* **[Lodestar](https://twitter.com/LodestarFinance)** | 20221211 | $4M | [SolidityFinance](https://twitter.com/SolidityFinance/status/1601684150456438784), [Lodestar](https://blog.lodestarfinance.io/post-mortem-summary-13f5fe0bb336) | [Transaction](https://arbiscan.io/tx/0xc523c6307b025ebd9aef155ba792d1ba18d5d83f97c7a846f267d3d9a3004e8c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Lodestar_exp.sol) | _

* **[MU&MUG](https://twitter.com/mucoinofficial)** | 20221210 | $57k | [BeosinAlert](https://twitter.com/BeosinAlert/status/1601422462012469248) | [Transaction](https://snowtrace.io/tx/0xab39a17cdc200c812ecbb05aead6e6f574712170eafbd73736b053b168555680) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/MUMUG_exp.sol) | _

* **[TIFIToken](https://twitter.com/TiFiToken)** | 20221210 | 87 WBNB | [PeckShield](https://twitter.com/peckshield/status/1601492605535399936) | [Transaction](https://bscscan.com/tx/0x1c5272ce35338c57c6b9ea710a09766a17bbf14b61438940c3072ed49bfec402) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/TIFI_exp.sol) | _

* **[AES (Deflationary token)]()** | 20221207 | $60k | [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1600442137811689473), [PeckShield](https://twitter.com/peckshield/status/1600418002163625984) | [Transaction](https://bscscan.com/tx/0xca4d0d24aa448329b7d4eb81be653224a59e7b081fc7a1c9aad59c5a38d0ae19) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/AES_exp.sol) | _

* **[BBOX](https://twitter.com/BBOXMetaverse)** | 20221205 | $12k | [AnciliaInc](https://twitter.com/AnciliaInc/status/1599599614490877952) | [Transaction](https://bscscan.com/tx/0xac57c78881a7c00dfbac0563e21b5ae3a8e3f9d1b07198a27313722a166cc0a3) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BBOX_exp.sol) | _

* **[APC](https://twitter.com/ArenaPlayAPC)** | 20221201 | $6k | [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1598262002010378241) | [Transaction](https://bscscan.com/tx/0xf2d4559aeb945fb8e4304da5320ce6a2a96415aa70286715c9fcaf5dbd9d7ed2) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/APC_exp.sol) | _

* **[INUKO](https://twitter.com/Inuko_Finance)** | 20221014 | $50k | [[AnciliaInc](https://twitter.com/AnciliaInc/status/1587848874076430336)] | [Transactions](https://bscscan.com/txs?a=0xb12011c14e087766f30f4569ccaf735ec2182165) | [POC](src/test/INUKO_exp.sol) | _

* **[ATK](https://twitter.com/)** | 20221012 | $127k | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1580095325200474112)] | [Transaction](https://bscscan.com/tx/0x601b8ab0c1d51e71796a0df5453ca671ae23de3d5ec9ffd87b9c378504f99c32) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ATK_exp.sol) | _

* **[ZoomproFinance](https://twitter.com/ZoomproFinance)** | 20220905 | $61,160 | [[blocksecteam](https://twitter.com/blocksecteam/status/1567027459207606273)] | [Transaction](https://bscscan.com/tx/0xe176bd9cfefd40dc03508e91d856bd1fe72ffc1e9260cd63502db68962b4de1a) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ZoomproFinance_exp.sol) | _

* **[ShadowFi](https://twitter.com/ShadowFi_)** | 20220902 | 1,078 BNB | [[PeckShieldAlert](https://twitter.com/PeckShieldAlert/status/1565549688509861888)] | [Transaction](https://bscscan.com/tx/0xe30dc75253eecec3377e03c532aa41bae1c26909bc8618f21fb83d4330a01018) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Shadowfi_exp.sol) | _

* **[EGD Finance](https://twitter.com/)** | 20220807 | 36,044 USDT | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1556483435388350464), [PeckShieldAlert](https://twitter.com/PeckShieldAlert/status/1556486817406283776)] | [Transaction](https://bscscan.com/tx/0x50da0b1b6e34bce59769157df769eb45fa11efc7d0e292900d6b0a86ae66a2b3) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/EGD-Finance.exp.sol) | _

### Reentrancy

* **[Curve](https://twitter.com/CurveFinance)** | 20230730 | $41M | [[LlamaRisk](https://hackmd.io/@LlamaRisk/BJzSKHNjn)] | [Transaction](https://etherscan.io/tx/0xa84aa065ce61dbb1eb50ab6ae67fc31a9da50dd2c74eefd561661bfce2f1620c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Curve_exp01.sol) | _JPEG_

* **[Paribus](https://twitter.com/paribus_io)** | 20230411 | $100k | [[Phalcon_xyz](https://twitter.com/Phalcon_xyz/status/1645742620897955842), [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1645744655357575170), [peckshield](https://twitter.com/peckshield/status/1645742296904929280)] | [Transaction](https://arbiscan.io/tx/0x0e29dcf4e9b211a811caf00fc8294024867bffe4ab2819cc1625d2e9d62390af) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Paribus_exp.sol) | _CompoundV2_

* **[Sentiment](https://twitter.com/sentimentxyz)** | 20230405 | $1M | [[peckshield](https://twitter.com/peckshield/status/1643417467879059456), [spreekaway](https://twitter.com/spreekaway/status/1643313471180644360), [Coinmonks](https://medium.com/coinmonks/theoretical-practical-balancer-and-read-only-reentrancy-part-1-d6a21792066c)] | [Transaction](https://arbiscan.io/tx/0xa9ff2b587e2741575daf893864710a5cbb44bb64ccdc487a100fa20741e0f74d) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Sentiment_exp.sol) | _Read-Only_

* **[dForce](https://twitter.com/dForcenet)** | 20230210 | ~$3.65M | [[SlowMist_Team](https://twitter.com/SlowMist_Team/status/1623956763598000129), [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1623901011680333824), [peckshield](https://twitter.com/peckshield/status/1623910257033617408)] | [Transaction](https://arbiscan.io/tx/0x5db5c2400ab56db697b3cc9aa02a05deab658e1438ce2f8692ca009cc45171dd) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/dForce_exp.sol) | _read-only_

* **[Orion Protocol](https://twitter.com/orion_protocol)** | 20230203 | $3M | [[peckshield](https://twitter.com/peckshield/status/1621337925228306433), [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1621263393054420992), [Numen Cyber](https://www.numencyber.com/analysis-of-orionprotocol-reentrancy-attack-with-poc/)] | [Transaction ETH](https://etherscan.io/tx/0xa6f63fcb6bec8818864d96a5b1bb19e8bd85ee37b2cc916412e720988440b2aa), [Transaction BSC](https://bscscan.com/tx/0xfb153c572e304093023b4f9694ef39135b6ed5b2515453173e81ec02df2e2104) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Orion_exp.sol) | _

* **[MidasCapital](https://twitter.com/MidasCapitalxyz)** | 20230116 | $650k | [[peckshield](https://twitter.com/peckshield/status/1614774855999844352), [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1614864084956254209)] | [Transaction](https://polygonscan.com/tx/0x0053490215baf541362fc78be0de98e3147f40223238d5b12512b3e26c0a2c2f) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Midas_exp.sol) | _read-only_

* **[JAY](https://twitter.com/jaypeggerz)** | 20221229 | $15.32 ETH | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1608372475225866240)] | [Transaction](https://etherscan.io/tx/0xd4fafa1261f6e4f9c8543228a67caf9d02811e4ad3058a2714323964a8db61f6) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/JAY_exp.sol) | _

* **[Defrost](https://twitter.com/Defrost_Finance)** | 20221223 | $170k | [[PeckShieldAlert](https://twitter.com/PeckShieldAlert/status/1606276020276891650)] | [Transaction](https://snowtrace.io/tx/0xc6fb8217e45870a93c25e2098f54f6e3b24674a3083c30664867de474bf0212d) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Defrost_exp.sol) | _

* **[DFXFinance](https://twitter.com/DFXFinance)** | 20221110 | $4M | [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1590960299246780417) | [Transaction](https://etherscan.io/tx/0x6bfd9e286e37061ed279e4f139fbc03c8bd707a2cdd15f7260549052cbba79b7) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/DFX_exp.sol) | _

* **[N00d Token](https://twitter.com/n00dleSwap)** | 20221026 | $29k | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1584959295829180416), [AnciliaInc](https://twitter.com/AnciliaInc/status/1584955717877784576)] | [Transaction](https://etherscan.io/tx/0x8037b3dc0bf9d5d396c10506824096afb8125ea96ada011d35faa89fa3893aea) | [POC](src/test/N00d_exp.sol) | _

* **[Market](https://www.market.xyz/)** | 20221024 | $220k | [[QuillAudits](https://quillaudits.medium.com/decoding-220k-read-only-reentrancy-exploit-quillaudits-30871d728ad5)] | [Transaction](https://polygonscan.com/tx/0xb8efe839da0c89daa763f39f30577dc21937ae351c6f99336a0017e63d387558) | [POC](src/test/Market_exp.t.sol) | _read-only_

* **[Thunder Brawl](https://twitter.com/THB_crypto)** | 20221001 | - | [[PeckShield](https://twitter.com/peckshield/status/1575890733373849601)] | [Transaction](https://bscscan.com/tx/0x57aa9c85e03eb25ac5d94f15f22b3ba3ab2ef60b603b97ae76f855072ea9e3a0) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/THB_exp.sol) | _

* **[Omni NFT](https://twitter.com/Omnimint_xyz)** | 20220710 | $1.4M | [[SlowMist_Team](https://twitter.com/SlowMist_Team/status/1546379086792388609)] | [Transaction](https://etherscan.io/tx/0x05d65e0adddc5d9ccfe6cd65be4a7899ebcb6e5ec7a39787971bcc3d6ba73996) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Omni_exp.sol) | _

* **[Rari Capital/Fei Protocol](https://twitter.com/RariCapital)** | 20220430 | $80 million | [[certik](https://certik.medium.com/fei-protocol-incident-analysis-8527440696cc), [peckshield](https://twitter.com/peckshield/status/1520369315698016256)] | [Transaction](https://etherscan.io/tx/0xab486012f21be741c9e674ffda227e30518e8a1e37a5f1d58d0b0d41f6e76530) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Rari_exp.t.sol) | _Flashloan Attack_

* **[Revest Finance](https://twitter.com/rena_finance)** | 20220327 | $11.2 million | [[BlockSecTeam](https://blocksecteam.medium.com/revest-finance-vulnerabilities-more-than-re-entrancy-1609957b742f)] | [[Transaction](https://etherscan.io/tx/0xe0b0c2672b760bef4e2851e91c69c8c0ad135c6987bbf1f43f5846d89e691428)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Revest_exp.sol) | _

* **[Hundred Finance](https://twitter.com/HundredFinance)** | 20220313 | $1.7 million | [[Immunefi](https://medium.com/immunefi/a-poc-of-the-hundred-finance-heist-4121f23a098)] | [[Transaction](https://gnosisscan.io/tx/0x534b84f657883ddc1b66a314e8b392feb35024afdec61dfe8e7c510cfac1a098)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/HundredFinance_exp.sol) | _ERC667_

* **[Paraluni](https://twitter.com/paraluni)** | 20220313 | $1.7 million | [[Halborn](https://halborn.com/explained-the-paraluni-hack-march-2022/)] [[PeckShield](https://twitter.com/peckshield/status/1502815435498176514)] | [[Transaction](https://bscscan.com/tx/0x70f367b9420ac2654a5223cc311c7f9c361736a39fd4e7dff9ed1b85bab7ad54)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Paraluni_exp.sol) | _


* **[Bacon Protocol](https://twitter.com/baconprotocol)** | 20220305 | $1 million | [[PeckShield](https://twitter.com/peckshield/status/1500105933128495108)] | [[Transaction1](https://etherscan.io/tx/0xacfcaa8e1c482148f9f2d592c78ca7a27934c7333dab31978ed0aef333a28ab6)] [[Transaction2](https://etherscan.io/tx/0x7d2296bcb936aa5e2397ddf8ccba59f54a178c3901666b49291d880369dbcf31)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Bacon_exp.sol) | _

* **[Visor Finance](https://twitter.com/VisorFinance)** | 20211221 | $8.2 million | [[BEOSIN](https://beosin.medium.com/two-vulnerabilities-in-one-function-the-analysis-of-visor-finance-exploit-a15735e2492)] | [[Transaction](https://etherscan.io/tx/0x69272d8c84d67d1da2f6425b339192fa472898dce936f24818fda415c1c1ff3f)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Visor_exp.t.sol) | _

* **[Cream Finance](https://twitter.com/CreamdotFinance)** | 20210830 | $18M | [[Twitter](https://twitter.com/peckshield/status/1432249600002478081)] | [[Transaction](https://etherscan.io/tx/0xa9a1b8ea288eb9ad315088f17f7c7386b9989c95b4d13c81b69d5ddad7ffe61e)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Cream_exp.sol) | _

* **[XSURGE](https://twitter.com/JimmyMc_XSURGE)** | 20210817 | $5M | [[Medium](https://medium.com/@Knownsec_Blockchain_Lab/knownsec-blockchain-lab-comprehensive-analysis-of-xsurge-attacks-c83d238fbc55)] | [[Transaction](https://bscscan.com/tx/0x8c93d6e5d6b3ec7478b4195123a696dbc82a3441be090e048fe4b33a242ef09d)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/XSURGE_exp.t.sol) | _

* **[RariCapital](https://twitter.com/RariCapital)** | 20210509 | $10M | [[Rekt](https://rekt.news/rari-capital-rekt/)] | [[Transaction](https://etherscan.com/tx/0x171072422efb5cd461546bfe986017d9b5aa427ff1c07ebe8acc064b13a7b7be)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/RariCapital_exp.sol) | _Cross Contract_

* **[Value Defi](https://twitter.com/value_defi)** | 20210508 | $11M | [[Rekt](https://rekt.news/value-rekt3/)] | [[Transaction](https://bscscan.com/tx/0xa00def91954ba9f1a1320ef582420d41ca886d417d996362bf3ac3fe2bfb9006)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ValueDefi_exp.sol) | _Cross Contract_


### Reflection token

* **BUNN** | 20230621 | $52BNB | [[DecurityHQ](https://twitter.com/DecurityHQ/status/1671803688996806656)] | [Transaction](https://bscscan.com/tx/0x24a68d2a4bbb02f398d3601acfd87b09f543d935fc24862c314aaf64c295acdb) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BUNN_exp.sol) | _

* **[OLIFE](https://twitter.com/OceanLifeToken)** | 20230419 | $32BNB | [[BeosinAlert](https://twitter.com/BeosinAlert/status/1648520494516420608)] | [Transaction](https://bscscan.com/tx/0xa21692ffb561767a74a4cbd1b78ad48151d710efab723b1efa5f1e0147caab0a) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/OLIFE_exp.sol) | _

* **[BIGFI](https://twitter.com/bigfinancetech)** | 20230322 | $30k | [[HypernativeLabs](https://twitter.com/HypernativeLabs/status/1638522680654675970)] | [Transaction](https://bscscan.com/tx/0x9fe19093a62a7037d04617b3ac4fbf5cb2d75d8cb6057e7e1b3c75cbbd5a5adc) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BIGFI_exp.sol) | _

* **[Sheep](https://twitter.com/sheeptokendefi)** | 20230210 | ~$3K | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1623999717482045440), [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1624077078852210691)] | [Transaction](https://bscscan.com/tx/0x61293c6dd5211a98f1a26c9f6821146e12fb5e20c850ad3ed2528195c8d4c98e) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Sheep_exp.sol) | _

* **FDP** | 20230207 | ~16 WBNB | [[BeosinAlert](https://twitter.com/BeosinAlert/status/1622806011269771266)] | [Transaction](https://bscscan.com/tx/0x09925028ce5d6a54801d04ff8f39e79af6c24289e84b301ddcdb6adfa51e901b) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/FDP_exp.t.sol) | _

* **TINU** | 20230126 | 22 ETH | [[libevm](https://twitter.com/libevm/status/1618718156343873536)] | [Transaction](https://etherscan.io/tx/0x6200bf5c43c214caa1177c3676293442059b4f39eb5dbae6cfd4e6ad16305668) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/TINU_exp.t.sol) | _

### K-value error
* **[Swapos V2]()** | 20230416 |  $468k | [[CertiK](https://twitter.com/CertiKAlert/status/1647530789947469825), [Beosin](https://twitter.com/BeosinAlert/status/1647552192243728385)] | [Transaction](https://etherscan.io/address/0x2df07c054138bf29348f35a12a22550230bd1405) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Swapos_exp.sol) | _

### ExchangeRate Manipulation & ERC4626 Inflation Attack
* **[HundredFinance](https://twitter.com/HundredFinance)** | 20230415 | $7M | [[PeckShield](https://twitter.com/peckshield/status/1647307128267476992), [DanielVF](https://twitter.com/danielvf/status/1647329491788677121), [Hexagate](https://twitter.com/hexagate_/status/1647334970258608131)] | [Transaction]() | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/HundredFinance_2_exp.sol) | _ERC4626_

### Misconfiguration

* **CS Token** | 20230524 | $714K | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1661098394130198528), [numencyber](https://twitter.com/numencyber/status/1661207123102167041)] | [Transaction](https://explorer.phalcon.xyz/tx/bsc/0x906394b2ee093720955a7d55bff1666f6cf6239e46bea8af99d6352b9687baa4) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/CS_exp.sol) | _Outdated global variable_

* **[yearnFinance](https://twitter.com/cmichelio/status/1646422861219807233)** | 20230413 | $11.6M | [[cmichelio](https://twitter.com/cmichelio/status/1646422861219807233), [Beosin](https://twitter.com/BeosinAlert/status/1646481687445114881)] | [Transaction]() | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/YearnFinance_exp.sol) | _

### Unrestricted Approval

* **[MetaPoint](https://twitter.com/MetaPoint1024)** | 20230412 | $820k(2500BNB) | [[PeckShieldAlert](https://twitter.com/PeckShieldAlert/status/1645980197987192833), [Phalcon_xyz](https://twitter.com/Phalcon_xyz/status/1645963327502204929)] | [Transaction](https://bscscan.com/tx/0x41853747231dcf01017cf419e6e4aa86757e59479964bafdce0921d3e616cc67) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/MetaPoint_exp.sol) | _


### public burn

* **[SafeMoon](https://twitter.com/safemoon)** | 20230328 | $8.9M | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1640894449122422784), [zokyo_io](https://twitter.com/zokyo_io/status/1641014520041840640)] | [Transaction](https://bscscan.com/tx/0x48e52a12cb297354a2a1c54cbc897cf3772328e7e71f51c9889bb8c5e533a934) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/safeMoon_exp.sol) | _frontruned_


### Yield Protocol Flaw

* **[Thena](https://twitter.com/ThenaFi_)** | 20230328 | $10k | [[LTV888](https://twitter.com/LTV888/status/1640563457094451214?t=OBHfonYm9yYKvMros6Uw_g&s=19)] | [Transaction](https://bscscan.com/tx/0x1ae499ccf292a2ee5e550702b81a4a7f65cd03af2c604e2d401d52786f459ba6) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Thena_exp.sol) | _




### Flashloan + scaledBalanceOf Manipulation

* **[ParaSpace NFT](https://twitter.com/ParaSpace_NFT)** | 20230317 | Rescued: ~2,909 ETH | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1636650252844294144)] | [Transaction](https://etherscan.io/tx/0xe3f0d14cfb6076cabdc9057001c3fafe28767a192e88005bc37bd7d385a1116a) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/paraspace_exp.sol), [POC 2](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Paraspace_exp_2.sol) | _


### Integer overflow

* **[Poolz](https://twitter.com/Poolz__)** | 20230315 | ~$390K | [[PeckShield](https://twitter.com/peckshield/status/1635860470359015425)] | [Transaction](https://bscscan.com/address/0x8bfaa473a899439d8e07bf86a8c6ce5de42fe54b) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/poolz_exp.sol) | _


### Storage Collision

* **[EFVault](https://www.shatacapital.com/)** | 20230224 | ~$5.1M | [[peckshield](https://twitter.com/peckshield/status/1630490333716029440), [drdr_zz](https://twitter.com/drdr_zz/status/1630500170373685248), [gbaleeeee](https://twitter.com/gbaleeeee/status/1630587522698080257)] | [Transaction](https://etherscan.io/tx/0x1fe5a53405d00ce2f3e15b214c7486c69cbc5bf165cf9596e86f797f62e81914) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/EFVault_exp.sol) | _


### Balance Recalculation Bug

* **[Spherax USDs](https://twitter.com/speraxusd)** | 20230203 | ~309k USDs (Stablecoin) | [[danielvf](https://twitter.com/danielvf/status/1621965412832350208), [Medium](https://medium.com/sperax/usds-feb-3-exploit-report-from-engineering-team-9f0fd3cef00c)] | [Transaction](https://arbiscan.io/tx/0xfaf84cabc3e1b0cf1ff1738dace1b2810f42d98baeea17b146ae032f0bdf82d5) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/USDs_exp.sol) | _

### Price Oracle Manipulation

* **[BonqDAO](https://twitter.com/BonqDAO)** | 20230202 | ~88M US$ | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1621043757390123008), [SlowMist_Team](https://twitter.com/SlowMist_Team/status/1621087651158966274)] | [Transaction 1](https://polygonscan.com/tx/0x31957ecc43774d19f54d9968e95c69c882468b46860f921668f2c55fadd51b19), [Transaction 2](https://polygonscan.com/tx/0xa02d0c3d16d6ee0e0b6a42c3cc91997c2b40c87d777136dedebe8ee0f47f32b1) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BonqDAO_exp.sol) | _

### Flashloan Price Oracle Manipulation
* **[NXUSD](https://twitter.com/nereusfinance)** | 20220906 | $50,000 | [[Medium](https://medium.com/nereus-protocol/post-mortem-flash-loan-exploit-in-single-nxusd-market-343fa32f0c6)] | [Transaction](https://snowtrace.io/tx/0x0ab12913f9232b27b0664cd2d50e482ad6aa896aeb811b53081712f42d54c026) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/NXUSD_exp.sol) | _

* **[PancakeBunny](https://hunny.finance/#/pools)** | 20210519 | $45M | [[Rekt](https://rekt.news/pancakebunny-rekt/)] | [[Transaction](https://bscscan.com/tx/0x897c2de73dd55d7701e1b69ffb3a17b0f4801ced88b0c75fe1551c5fcce6a979)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/PancakeBunny_exp.sol) | _


### Incorrect Parameter Setting

* **[UFDao](https://twitter.com/xdaoapp)** | 20230112 | $90k | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1613507804412940289)] | [Transaction](https://bscscan.com/tx/0x933d19d7d822e84e34ca47ac733226367fbee0d9c0c89d88d431c4f99629d77a) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/UFDao_exp.sol) | Incorrect Parameter Setting

### Insufficient Validation + FlashLoan

* **DFS** | 20221230 | $1450 | [[CertiKAlert](https://twitter.com/CertiKAlert/status/1608788290785665024)] | [Transaction](https://bscscan.com/tx/0xcddcb447d64c2ce4b3ac5ebaa6d42e26d3ed0ff3831c08923c53ea998f598a7c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/DFS_exp.sol) | Insufficient Validation + FlashLoan





### Malicious Unlimted Minting

* **[NOVAToken](https://twitter.com/nova_token)** | 20221209 | 330 $BNB | [BeosinAlert](https://twitter.com/BeosinAlert/status/1601168659585454081) | [Transaction](https://bscscan.com/tx/0xf743dba906255cf6f75f8243ef8192f2a211aacf03df99322584686b5c445c23) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/NovaExchange_exp.sol) | _Rugged_

### Predicting Random Numbers
* **[RFB](https://twitter.com/RoastFootball)** | 20221205 | 12 BNB | [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1599991294947778560) | [Transaction](https://bscscan.com/tx/0xcc8fdb3c6af8bb9dfd87e913b743a13bbf138a143c27e0f387037887d28e3c7a) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/RFB_exp.sol) | _

### FlashLoan Attack

* **[OverNight](https://twitter.com/overnight_fi)** | 20221202 | $170k | [PeckShield](https://twitter.com/peckshield/status/1598704809690877952) | [Transaction](https://snowtrace.io/tx/0xf10807f9a675dd2db9a45e39f37c68a4116006f9a40e97a68c145e3859557809) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Overnight_exp.sol) | _

* **[UEarnPool](https://bscscan.com/tx/0xb83f9165952697f27b1c7f932bcece5dfa6f0d2f9f3c3be2bb325815bfd834ec)** | 20221117 | $24k | [CertiKAlert](https://twitter.com/CertiKAlert/status/1593094922160128000) | [Transaction](https://bscscan.com/tx/0x824de0989f2ce3230866cb61d588153e5312151aebb1e905ad775864885cd418) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/UEarnPool_exp.sol) | _

* **[NewFreeDAO](https://twitter.com/)** | 20220908 | $1,000,000 | [[SlowMist_Team](https://twitter.com/SlowMist_Team/status/1567854876633309186)] | [Transaction](https://bscscan.com/tx/0x1fea385acf7ff046d928d4041db017e1d7ead66727ce7aacb3296b9d485d4a26) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/NewFreeDAO_exp.sol) | _

* **[DODO](https://dodoex.io/zh)** | 20210308 | $700K | [[Postmortem](https://blog.dodoex.io/dodo-pool-incident-postmortem-with-a-little-help-from-our-friends-327e66872d42)] | [[Transaction](https://etherscan.io/tx/0x395675b56370a9f5fe8b32badfa80043f5291443bd6c8273900476880fb5221e)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/dodo_flashloan_exp.sol) | _

### Business Logic Flaw & Access Control

* **[MBC](https://twitter.com/Moonbirds_Club)** | 20221129 | $5.6k | [AnciliaInc](https://twitter.com/AnciliaInc/status/1597742575623888896) | [Address](https://bscscan.com/address/0x4e87880a72f6896e7e0a635a5838ffc89b13bd17) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/MBC_exp.sol) | _

### Protocol Token Incompatible
* **[NUM](https://twitter.com/numbersprotocol)** | 20221123 | $13k | [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1595346020237352960) | [Transaction](https://etherscan.io/tx/0x8a8145ab28b5d2a2e61d74c02c12350731f479b3175893de2014124f998bff32) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/NUM_exp.sol) | _ 

### Lack of Permission Check

* **[AUR](https://twitter.com/AURofficial_)** | 20221122 | $13k | [AnciliaInc](https://twitter.com/AnciliaInc/status/1595142246570958848) | [Transaction](https://bscscan.com/tx/0x7f031e8543e75bd5c85168558be89d2e08b7c02a32d07d76517cdbb10e279782) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/AUR_exp.sol) | _

### Verify FlashLoan Callback

* **[AnnexFinance](https://twitter.com/AnnexFinance)** | 20221119 | $3k | [AnciliaInc](https://twitter.com/AnciliaInc/status/1593690338526273536) | [Transaction](https://bscscan.com/tx/0x3757d177482171dcfad7066c5e88d6f0f0fe74b28f32e41dd77137cad859c777) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Annex_exp.sol) | _


* **[EFLeverVault](https://twitter.com/EarningFarm)** | 20221014 | 750 ETH | [[Supremacy_CA](https://twitter.com/Supremacy_CA/status/1581012823701786624), [MevRefund](https://twitter.com/MevRefund/status/1580917351217627136), [danielvf](https://twitter.com/danielvf/status/1580936010556661761)] | [Transaction](https://etherscan.io/tx/0x160c5950a01b88953648ba90ec0a29b0c5383e055d35a7835d905c53a3dda01e) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/EFLeverVault_exp.sol) | _


### Price-caching Design Defect

* **[Kashi](https://twitter.com/SushiSwap)** | 20221108 | $110k | [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1603633067876155393) | [Transaction](https://etherscan.io/tx/0x3d163bfbec5686d428a6d43e45e2626a220cc4fcfac7620c620b82c1f2537c78) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Kashi_exp.sol) | _


### Incorrect Reward Calculation

* **[VTF Token](https://twitter.com/)** | 20221027 | $50k | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1585575129936977920), [peckshield](https://twitter.com/peckshield/status/1585572694241988609), [BeosinAlert](https://twitter.com/BeosinAlert/status/1585587030981218305)] | [Transaction 1](https://bscscan.com/tx/0xeeaf7e9662a7488ea724223c5156e209b630cdc21c961b85868fe45b64d9b086), [Transaction 2](https://bscscan.com/tx/0xc2d2d7164a9d3cfce1e1dac7dc328b350c693feb0a492a6989ceca7104eef9b7) | [POC](src/test/VTF_exp.sol) | Incorrect Reward Calculation

### Liquidity Migration Exploit

* **[Team Finance](https://twitter.com/TeamFinance_)** | 20221027 | Multiple Tokens ~$15.8M US$ | [[TeamFinance_](https://twitter.com/TeamFinance_/status/1585770918873542656), [peckshield](https://twitter.com/peckshield/status/1585587858978623491), [solid_group_1](https://twitter.com/solid_group_1/status/1585643249305518083), [BeosinAlert](https://twitter.com/BeosinAlert/status/1585578499125178369)] | [Transaction](https://etherscan.io/tx/0xb2e3ea72d353da43a2ac9a8f1670fd16463ab370e563b9b5b26119b2601277ce) | [POC](src/test/TeamFinance.exp.sol) | Liquidity Migration Exploit


### Transfer Logic Flaw

* **[HEALTH](https://twitter.com/)** | 20221020 | 16 BNB | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1583073442433495040)] | [Transaction](https://bscscan.com/tx/0xae8ca9dc8258ae32899fe641985739c3fa53ab1f603973ac74b424e165c66ccf) | [POC](src/test/HEALTH_exp.sol) | Transfer Logic Flaw

* **[PLTD](https://twitter.com/)** | 20221018 | $24k | [[BeosinAlert](https://twitter.com/BeosinAlert/status/1582181583343484928)] | [Transaction](https://bscscan.com/tx/0x8385625e9d8011f4ad5d023d64dc7985f0315b6a4be37424c7212fe4c10dafe0) | [POC](src/test/PLTD_exp.sol) | Transfer Logic Flaw

### Incorrect signature verification

* **[BEGO](https://twitter.com/GeoDataBlock)** | 20221020 | 12 BNB | [[AnciliaInc](https://twitter.com/AnciliaInc/status/1582828751250784256), [peckshield](https://twitter.com/peckshield/status/1582892058800685058)] | [Transaction](https://bscscan.com/tx/0x9f4ef3cc55b016ea6b867807a09f80d1b2e36f6cd6fccfaf0182f46060332c57) | [POC](src/test/BEGO_exp.sol) | Incorrect signature verification

### MEVBOT a47b
* **[MevRefund](https://twitter.com/MevRefund)** | 20221014 | $241k | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1580779311862190080), [AnciliaInc](https://twitter.com/AnciliaInc/status/1580705036400611328)] | [Transaction](https://etherscan.io/tx/0x35ecf595864400696853c53edf3e3d60096639b6071cadea6076c9c6ceb921c1) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/MEVa47b_exp.sol) | _


### Public FunctionCall
* **[Carrot](https://twitter.com/)** | 20221010 | >$31k | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1579908411235237888)] | [Transaction](https://bscscan.com/tx/0xa624660c29ee97f3f4ebd36232d8199e7c97533c9db711fa4027994aa11e01b9) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Carrot_exp.sol) | _

### Malicious Proposal Mint & Transfer Ownership
* **[XaveFinance](https://twitter.com/XaveFinance)** | 20221009 | >$590w | [[BeosinAlert](https://twitter.com/BeosinAlert/status/1579040051853303808)] | [Transaction](https://etherscan.io/tx/0xc18ec2eb7d41638d9982281e766945d0428aaeda6211b4ccb6626ea7cff31f4a) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/XaveFinance_exp.sol) | _

### Incorrect Owner Address Validation
* **[TransitFinance](https://twitter.com/TransitFinance)** | 20221002 | - | [[TransitFinance](https://twitter.com/TransitFinance/status/1576463550557483008), [1nf0s3cpt](https://twitter.com/1nf0s3cpt/status/1576511552592543745)] | [Transaction](https://bscscan.com/tx/0x181a7882aac0eab1036eedba25bc95a16e10f61b5df2e99d240a16c334b9b189) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/TransitSwap_exp.sol) | _


### Incorrect Reward Calculation
* **[RL Token](https://twitter.com/)** | 20221001 | - | [[CertiKAlert](https://twitter.com/CertiKAlert/status/1576195971003858944)] | [Transaction](https://bscscan.com/tx/0xe15d261403612571edf8ea8be78458b88989cf1877f0b51af9159a76b74cb466) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/RL_exp.sol) | _

* **[DPC](https://twitter.com/DPCProtocol)** | 20220910 | $103,755 | [[BeosinAlert](https://twitter.com/BeosinAlert/status/1568429355919089664), [LearnBlockchain](https://learnblockchain.cn/article/4733)] | [Contract Address](https://bscscan.com/address/0x2109bbecB0a563e204985524Dd3DB2F6254AB419) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/DPC_exp.sol) | _

### MEV-Badc0de
* **[MEVBOT](https://twitter.com/)** | 20220928 | $1,469,700 | [[RektNews](https://rekt.news/ripmevbot/)] | [Transaction](https://etherscan.io/tx/0x59ddcf5ee5c687af2cbf291c3ac63bf28316a8ecbb621d9f62d07fa8a5b8ef4e) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/MEVbadc0de_exp.sol) | _

### MevBot Private Tx
* **[MevBot](https://twitter.com/)** | 20220913 | $140 K | [[BlockSecTeam](https://blocksecteam.medium.com/the-two-sides-of-the-private-tx-service-on-binance-smart-chain-a76917c3ce51), [1nf0s3cpt](https://twitter.com/1nf0s3cpt/status/1577594615104172033)] | [Transaction](https://bscscan.com/tx/0xd48758ef48d113b78a09f7b8c7cd663ad79e9965852e872fdfc92234c3e598d2) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BNB48MEVBot_exp.sol) |  _

### Pair Manipulation

* **[RES-Token](https://twitter.com/)** | 20221006 | - | [[AnciliaInc](https://twitter.com/AnciliaInc/status/1578119778446680064)] | [Transaction](https://bscscan.com/tx/0xe59fa48212c4ee716c03e648e04f0ca390f4a4fc921a890fded0e01afa4ba96d) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/RES_exp.sol), [POC2](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/RES02_exp.sol) | _

* **[RADT-DAO](https://twitter.com/)** | 20220923 | 94,304 USDT | [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1573252869322846209) | [Transaction](https://bscscan.com/tx/0xd692f71de2768017390395db815d34033013136c378177c05d0d46ef3b6f0897) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/RADT_exp.sol) |  _

* **[YYDS](https://twitter.com/yyds_token)** | 20220909 | $742,286.27 | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1567928377432051713)] | [Transaction](https://bscscan.com/tx/0x04a1f0d1694242515ecb14faa71053901f11a1286cd21c27fe5542f9eeb62356) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Yyds_exp.sol) | _




### Predicting Random Numbers
* **[LuckyTiger NFT](https://opensea.io/collection/lzclub-luckytiger)** | 20220824 | 50 NFTs | [[1nf0s3cpt](https://twitter.com/1nf0s3cpt/status/1576117129589317633)] | [Transaction](https://etherscan.io/tx/0x804ff3801542bff435a5d733f4d8a93a535d73d0de0f843fd979756a7eab26af) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/LuckyTiger_exp.sol) | _

### Incorrect Logic Check
* **[XSTABLE Protocol](https://xstable.finance/)** | 20220810 | 27.13 WETH | [[BlockSecTeam](https://mobile.twitter.com/BlockSecTeam/status/1557195012042936320)] | [Transaction](https://etherscan.io/tx/0x873f7c77d5489c1990f701e9bb312c103c5ebcdcf0a472db726730814bfd55f3) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/XST.exp.sol) | _

### Skim token balance
* **[ANCH](https://twitter.com)** | 20220809 | - | [[AnciliaInc](https://twitter.com/AnciliaInc/status/1557527183966408706)] | [Contract](https://bscscan.com/address/0xa4f5d4afd6b9226b3004dd276a9f778eb75f2e9e#code) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ANCH_exp.sol) | _


### Incorrect acceptable merkle-root checks
* **[Nomad Bridge](https://app.nomad.xyz/)** | 20220802 | Multiple ERC-20 Tokens (~152M US$) | [[samczsun](https://twitter.com/samczsun/status/1554252024723546112)] | [Transaction](https://etherscan.io/tx/0xa5fe9d044e4f3e5aa5bc4c0709333cd2190cba0f4e7f16bcf73f49f83e4a5460) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/NomadBridge.exp.sol) | _

### Lack of access control mechanism
* **[Reaper Farm](https://twitter.com/Reaper_Farm)** | 20220801 | Multiple ERC-20 Tokens (~1.7M US$) | [[Reaper_Farm](https://twitter.com/Reaper_Farm/status/1554500909740302337), [BeosinAlert](https://twitter.com/BeosinAlert/status/1554476940593340421)] | [Transaction](https://ftmscan.com/tx/0xc92ls9f3b9312ff26be0adb1c3ff832dbdafdcbcaad33d002744effd515e53c9d5) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ReaperFarm.exp.sol) | _

### Incorrect recipient balance check, did not check sender!=recipient in transfer
* **[LPC](https://twitter.com/)** | 20220725 | 178 BNB (~45,715 US$) | [[panewslab](https://www.panewslab.com/zh_hk/articledetails/uwv4sma2.html), [BeosinAlert](https://twitter.com/BeosinAlert/status/1551535854681718784)] | [Transaction](https://bscscan.com/tx/0x0e970ed84424d8ea51f6460ce6105ab68441d4450a80bc8d749fdf01e504ed8c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/LPC.exp.sol) | _

### Storage Collision & Malicious Proposal
* **[Audius](https://twitter.com/AudiusProject)** | 20220723 | 704 ETH (~1.08M US$) | [[AudiusProject](https://twitter.com/AudiusProject/status/1551000725169180672), [1nf0s3cpt](https://twitter.com/1nf0s3cpt/status/1551050841146400768)] | [Contract](https://etherscan.io/address/0xbdbb5945f252bc3466a319cdcc3ee8056bf2e569) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Audius.exp.sol) | _

### Flashloans & Price Manipulation (FlashLoan price manipulation)
* **[SpaceGodzilla](https://mobile.twitter.com/SpaceGodzilla_c)** | 20220713 | 25,378 BUSD | [[BlockSecTeam](https://mobile.twitter.com/BlockSecTeam/status/1547456591900749824)] | [Transaction](https://bscscan.com/tx/0x7f183df11f1a0225b5eb5bb2296b5dc51c0f3570e8cc15f0754de8e6f8b4cca4) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SpaceGodzilla.exp.sol) | _

* **[Wault Finance](https://twitter.com/Wault_Finance)** | 20210804 | 390 ETH | [[Medium](https://medium.com/@Knownsec_Blockchain_Lab/wault-finance-flash-loan-security-incident-analysis-368a2e1ebb5b)] | [[Transaction](https://bscscan.com/tx/0x31262f15a5b82999bf8d9d0f7e58dcb1656108e6031a2797b612216a95e1670e)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/WaultFinance_exp.sol) | _


### Optimism NFT Marketplace
* **[Quixotic](https://twitter.com/quixotic_io)** | 20220701 | $100K | [[1nf0s3cpt](https://twitter.com/1nf0s3cpt/status/1542808565349777408), [SlowMist_Team](https://twitter.com/SlowMist_Team/status/1542795627603857409)] | [Transaction](https://optimistic.etherscan.io/tx/0x5dc519726e1236eb846271f6699e03cdd1a8fd593a2900c71cd2aabbdb7c92e6) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Quixotic_exp.sol) | _

### Infinite Number of Loans
* **[XCarnival](https://twitter.com/XCarnival_Lab)** | 20220626 | 3087 ETH (~$3.87M) | [[XCarnival_Lab](https://twitter.com/XCarnival_Lab/status/1541226298399653888), [peckshield](https://twitter.com/peckshield/status/1541047171453034501), [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1541070850505723905)] | [Transaction](https://etherscan.io/tx/0x51cbfd46f21afb44da4fa971f220bd28a14530e1d5da5009cfbdfee012e57e35) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/XCarnival.exp.sol) | _

### Private key compromised
* **[Harmony's Horizon Bridge](https://twitter.com/harmonyprotocol)** | 20220624 | $100 million | [[harmonyprotocol](https://twitter.com/harmonyprotocol/status/1540110924400324608), [0xIvo](https://twitter.com/0xIvo/status/1540165571681128448), [1nf0s3cpt](https://twitter.com/1nf0s3cpt/status/1540139812715261952)] | [Transaction](https://etherscan.io/tx/0x6487952d46b5265f56ec914fcff1a3d45d76f77e2407f840bdf264a5a7459100) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Harmony_multisig.sol) | _


### Flashloan & Price Oracle Manipulation

* **[BXH](https://twitter.com/BXH_Blockchain)** | 20220928 | $40,305 | [[Jinse](https://www.jinse.com/lives/319392.html)] | [Transaction](https://bscscan.com/tx/0xa13c8c7a0c97093dba3096c88044273c29cebeee109e23622cd412dcca8f50f4) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BXH_exp.sol) | _

* **[InverseFinance](https://twitter.com/InverseFinance)** | 20220616 | 53.2445 WBTC and 99,976.29 USDT | [[peckshield](https://twitter.com/peckshield/status/1537382891230883841), [SlowMist_Team](https://twitter.com/SlowMist_Team/status/1537602909512376321), [blocksecteam](https://blocksecteam.medium.com/price-oracle-manipulation-attack-on-inverse-finance-a5544218ea91), [certik](https://www.certik.com/resources/blog/6LbL57WA3iMNm8zd7q111R-inverse-finance-incident-analysis)] | [Transaction](https://etherscan.io/tx/0x958236266991bc3fe3b77feaacea120f172c0708ad01c7a715b255f218f9313c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/InverseFinance_exp.sol) | _

* **[Discover](https://twitter.com/)** | 20220606 | 49 BNB | [[BeosinAlert](https://www.twitter.com/BeosinAlert/status/1533734518623899648), [anquanke](https://www.anquanke.com/post/id/274003)] | [Transaction](https://bscscan.com/tx/0x8a33a1f8c7af372a9c81ede9e442114f0aabb537e5c3a22c0fd7231c4820f1e9) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Discover_exp.sol) | _

* **[OneRing Finance](https://twitter.com/Onering_Tools)** | 20220321 | $1.45 million | [[OneRingFinance](https://medium.com/oneringfinance/onering-finance-exploit-post-mortem-after-oshare-hack-602a529db99b)] | [[Transaction](https://ftmscan.com/tx/0xca8dd33850e29cf138c8382e17a19e77d7331b57c7a8451648788bbb26a70145)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/OneRing_exp.sol) | _

* **[NOVO Protocol](https://twitter.com/novodefi)** | 20220529 | 279 BNB | [[panewslab](https://www.panewslab.com/zh_hk/articledetails/f40t9xb4.html), [BscScan](https://bscscan.com/address/0xa0787daad6062349f63b7c228cbfd5d8a3db08f1#code)] | [Transaction](https://bscscan.com/tx/0xc346adf14e5082e6df5aeae650f3d7f606d7e08247c2b856510766b4dfcdc57f) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Novo_exp.sol) | _

* **[DEUS DAO](https://twitter.com/DeusDao)** | 20220428 | $13 million | [[peckshield](https://twitter.com/peckshield/status/1519531866109317121)] | [Transaction](https://ftmscan.com/tx/0xe374495036fac18aa5b1a497a17e70f256c4d3d416dd1408c026f3f5c70a3a9c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/deus_exp.sol) | _

* **[ElephantMoney](https://twitter.com/ElephantStatus)** | 20220412 | $11.2 million (27,416.46 BNB) | [[ElephantMoney](https://medium.com/elephant-money/reserve-exploit-52fd36ccc7e8)] [[peckshield](https://twitter.com/peckshield/status/1514023036596330496)] [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1513966074357698563)]| [[Transaction](https://bscscan.com/tx/0xec317deb2f3efdc1dbf7ed5d3902cdf2c33ae512151646383a8cf8cbcd3d4577)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Saddle_exp.sol) | _

### Signature replay
* **[Wintermute](https://twitter.com/wintermute_t)** | 20220608 | 20 million Optimism (OP) tokens (returned 17 million) | [[inspexco](https://inspexco.medium.com/how-20-million-op-was-stolen-from-the-multisig-wallet-not-yet-owned-by-wintermute-3f6c75db740a)] | [Transaction1](https://optimistic.etherscan.io/tx/0x75a42f240d229518979199f56cd7c82e4fc1f1a20ad9a4864c635354b4a34261), [Transaction2](https://optimistic.etherscan.io/tx/0x00a3da68f0f6a69cb067f09c3f7e741a01636cbc27a84c603b468f65271d415b) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Optimism_exp.sol) | _

### Skim token balance
* **[HackDao](https://twitter.com/)** | 20220524 | 279 BNB | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1529084919976034304)] | [Transaction](https://bscscan.com/tx/0x04673c95054247588bb8380dbc7d361f08f8f0baa319366f48ad46e51d08422d) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/HackDao_exp.sol) | _

### Flashloan
* **[NFTX protocol ApeCoin (APE)](https://twitter.com/)** | 20220517 | $1.1 million | [[coincu](https://news.coincu.com/73892-the-flashloan-attack-on-the-ape-airdrop-to-claim-1-1-million-of-ape-tokens/)] | [Transaction](https://etherscan.io/tx/0xeb8c3bebed11e2e4fcd30cbfc2fb3c55c4ca166003c7f7d319e78eaab9747098) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Bayc_apecoin_exp.sol) | _

* **[Wiener DOGE](https://twitter.com/WienerDogeBSC)** | 20220424 | 78 BNB | [[coinyuppie](https://coinyuppie.com/four-combinations-of-hackers-analysis-of-attacks-on-wiener-doge-last-kilometer-medamon-and-pidao-projects/), [solid_group](https://twitter.com/solid_group_1/status/1519034573354676224)] | [Transaction](https://bscscan.com/tx/0x4f2005e3815c15d1a9abd8588dd1464769a00414a6b7adcbfd75a5331d378e1d) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Wdoge_exp.sol) | _

### Malicious Proposal & Price Oracle Manipulation
* **[Fortress Loans](https://twitter.com/Fortressloans)** | 20220508 | 1,048.1 ETH + 400,000 DAI (~$3.00M) | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1523530484877209600), [Certik](https://www.certik.com/resources/blog/k6eZOpnK5Kdde7RfHBZgw-fortress-loans-exploit)] | [Transaction](https://bscscan.com/tx/0x13d19809b19ac512da6d110764caee75e2157ea62cb70937c8d9471afcb061bf) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/FortressLoans.exp.sol) | _

### Swap Metapool Attack
* **[Saddle Finance](https://twitter.com/saddlefinance)** | 20220430 | $10 million | [[peckshield](https://twitter.com/peckshield/status/1520330006710616064), [medium](https://medium.com/immunefi/hack-analysis-saddle-finance-april-2022-f2bcb119f38), [github](https://github.com/Hephyrius/Immuni-Saddle-POC)] | [Transaction1](https://etherscan.io/tx/0x2b023d65485c4bb68d781960c2196588d03b871dc9eb1c054f596b7ca6f7da56), [Transaction2](https://etherscan.io/tx/0xe7e0474793aad11875c131ebd7582c8b73499dd3c5a473b59e6762d4e373d7b8) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Saddle_exp.sol) | _



### Denial of Service
* **[Akutar NFT](https://twitter.com/AkuDreams)** | 20220423 | 34M USD | [[blocksecteam](https://blocksecteam.medium.com/how-akutar-nft-loses-34m-usd-60d6cb053dff), [bscscan](https://bscscan.com/tx/0x0507476234193a9a5c7ae2c47e4c4b833a7c3923cefc6fd7667b72f3ca3fa83a)] | [Contract](https://etherscan.io/address/0xf42c318dbfbaab0eee040279c6a2588fa01a961d#code) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/AkutarNFT_exp.sol) | _

### Reward distribution flaw
* **[Zeed Finance](https://twitter.com/zeedcommunity)** | 20220421 | $1 million | [[cryptotimes](https://www.cryptotimes.io/hacker-leaves-1m-to-self-destruct-after-zeed-protocol-exploit/), [zeedcommunity](https://medium.com/@zeedcommunity/the-solution-for-the-yeed-lp-pool-attack-a120c53948cd)] | [Contract](https://bscscan.com/address/0x05e55d051ac0a5fb744e71704a8fa4ee3b103374) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Zeed_exp.sol) | _

### DAO + Flashloan
* **[BeanstalkFarms](https://twitter.com/BeanstalkFarms)** | 20220416 | $182 million | [[rekt](https://rekt.news/beanstalk-rekt/), [uno-re](https://medium.com/uno-re/beanstalk-farms-hacked-total-damage-is-182-million-b699dd3e5c8), [peckshield](https://twitter.com/peckshield/status/1515680335769456640)] | [Transaction 1](https://etherscan.io/tx/0x68cdec0ac76454c3b0f7af0b8a3895db00adf6daaf3b50a99716858c4fa54c6f), [Transaction 2](https://etherscan.io/tx/0xcd314668aaa9bbfebaf1a0bd2b6553d01dd58899c508d4729fa7311dc5d33ad7) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Beanstalk_exp.sol) | _

### Access control & Price Oracle Manipulation
* **[Rikkei Finance](https://twitter.com/RikkeiFinance)** | 20220415 | $1.1 million (2671 BNB) | [[blockmagnates](https://blockmagnates.com/rikkei-finance-hack/), [knownseclab](https://knownseclab.com/news/625e865cf1c544005a4bdaf2), [rikkeifinance](https://rikkeifinance.medium.com/rikkei-finance-incident-investigation-report-b5b1745b0155)] | [Transaction](https://bscscan.com/tx/0x93a9b022df260f1953420cd3e18789e7d1e095459e36fe2eb534918ed1687492) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Rikkei_exp.sol) | _

### Creat Future
* **[CreatFuture](https://twitter.com/)** | 20220411 | $1.9 million | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1556497016016228358)] | [[Transaction](https://bscscan.com/tx/0xc7647406542f8f2473a06fea142d223022370aa5722c044c2b7ea030b8965dd0)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/cftoken_exp.sol) | _

### Flashloan + token migrate flaw
* **[GYMNetwork](https://gymdefi.io/)** | 20220409 | 1,327 WBNB | [[BlockSecTeam](https://twitter.com/BlockSecTeam/status/1512832398643265537)] [[Beosin](https://medium.com/@Beosin_com/beosin-analysis-of-the-attack-on-gymdefi-e5a23bfd93fe)] | [[Transaction](https://bscscan.com/tx/0xa5b0246f2f8d238bb56c0ddb500b04bbe0c30db650e06a41e00b6a0fff11a7e5)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Gym_1_exp.sol) | _

### Ronin Network - Bridge
* **[Ronin Network](https://twitter.com/Ronin_Network)** | 20220329 | $624 million | [[Rekt News](https://rekt.news/ronin-rekt/)] | [[Transaction 1](https://etherscan.io/tx/0xc28fad5e8d5e0ce6a2eaf67b6687be5d58113e16be590824d6cfa1a94467d0b7)] [[Transaction 2](https://etherscan.io/tx/0xed2c72ef1a552ddaec6dd1f5cddf0b59a8f37f82bdda5257d9c7c37db7bb9b08)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Ronin_exp.sol) | _

### Custom Approval Logic
* **[Redacted Cartel](https://twitter.com/redactedcartel)** | 20220329 | - | [[Immunefi](https://medium.com/immunefi/redacted-cartel-custom-approval-logic-bugfix-review-9b2d039ca2c5)] | [[Contract Address](https://bscscan.com/address/0x9ee1873ba8383B1D4ac459aBd3c9C006Eaa8800A)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/RedactedCartel_exp.sol) | _

### Auctus
* **[Auctus](https://twitter.com/AuctusOptions)** | 20220326 | $726k | [[AuctusOptions](https://twitter.com/AuctusOptions/status/1508647849663291398?cxt=HHwWjICzpbzO5e8pAAAA)] | [[Transaction](https://etherscan.io/tx/0x2e7d7e7a6eb157b98974c8687fbd848d0158d37edc1302ea08ee5ddb376befea)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Auctus_exp.sol) | _

### CompoundTUSD SweepTokenBypass
* **[Compound Finance](https://twitter.com/compoundfinance)** | 20220322 | - | [[OpenZeppelin](https://blog.openzeppelin.com/compound-tusd-integration-issue-retrospective/)] | [[Contract Address](https://etherscan.io/address/0x8dd5fbCe2F6a956C3022bA3663759011Dd51e73E)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/CompoundTusd_exp.sol) | _



### Bridges
* **[Li.Fi](https://twitter.com/lifiprotocol)** | 20220320 | $570K | [[lifiprotocol](https://twitter.com/lifiprotocol/status/1505738407938387971)] [[Blog](https://blog.li.fi/20th-march-the-exploit-e9e1c5c03eb9)] | [[Transaction](https://etherscan.io/tx/0x4b4143cbe7f5475029cf23d6dcbb56856366d91794426f2e33819b9b1aac4e96)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/LiFi_exp.sol) | _

### Underflow
* **[Umbrella Network](https://twitter.com/UmbNetwork)** | 20220320 | $4.26 billion | [[Umbrella Network](https://medium.com/uno-re/umbrella-network-hacked-700k-lost-97285b69e8c7)] | [[Transaction](https://etherscan.io/tx/0x33479bcfbc792aa0f8103ab0d7a3784788b5b0e1467c81ffbed1b7682660b4fa)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Umbrella_exp.sol) | _


* **[Grim Finance](https://twitter.com/FinanceGrim)** | 20211218 | $30 million | [[Cointelegraph](https://cointelegraph.com/news/defi-protocol-grim-finance-lost-30m-in-5x-reentrancy-hack)] | [[Transaction](https://ftmscan.com/tx/0x19315e5b150d0a83e797203bb9c957ec1fa8a6f404f4f761d970cb29a74a5dd6)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Grim_exp.sol) | _

### Business logic in mint()
* **[Fantasm Finance](https://twitter.com/fantasm_finance)** | 20220309 | $2.6 million | [[Fantasm](https://twitter.com/fantasm_finance/status/1501569232881995785)] [[QuillHash](https://medium.com/quillhash/fantom-based-protocol-fantasm-suffers-2-6m-exploit-32de8191ccd4)] | [[Transactions](https://ftmscan.com/address/0x47091e015b294b935babda2d28ad44e3ab07ae8d#tokentxns)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Fantasm_exp.sol) | _

### Zero Fee
* **[TreasureDAO](https://twitter.com/Treasure_DAO)** | 20220303 | $1 million | [[SlowMist](https://slowmist.medium.com/analysis-of-the-treasuredao-zero-fee-exploit-73791f4b9c14)] | [[Transaction](https://arbiscan.io/tx/0x82a5ff772c186fb3f62bf9a8461aeadd8ea0904025c3330a4d247822ff34bc02)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/TreasureDAO_exp.sol) | _

### DAO
* **[BuildFinance](https://twitter.com/finance_build)** | 20220214 | $470k | [[CryptoTimes](https://www.cryptotimes.io/build-finance-suffered-hostile-governance-takeover-lost-470k/)] | [[Transaction](https://etherscan.io/tx/0x544e5849b71b98393f41d641683586d0b519c46a2eeac9bcb351917f40258a85)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BuildF_exp.sol) | _


### Bridge
* **[Meter](https://twitter.com/Meter_IO)** | 20220206 | $4.3 million | [[ChainSafe Blog](https://blog.chainsafe.io/breaking-down-the-meter-io-hack-a46a389e7ae4)] | [[Transaction](https://moonriver.moonscan.io/tx/0x5a87c24d0665c8f67958099d1ad22e39a03aa08d47d00b7276b8d42294ee0591)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/meter_exp.sol) | _

### Bridge address(0).safeTransferFrom() does not revert
* **[Qubit Finance](https://twitter.com/QubitFin)** | 20220128 | $80 million | [[REKT](https://rekt.news/qubit-rekt/)] | [[Transaction 1](https://etherscan.io/tx/0xac7292e7d0ec8ebe1c94203d190874b2aab30592327b6cc875d00f18de6f3133)] [[Transaction 2](https://bscscan.com/tx/0x50946e3e4ccb7d39f3512b7ecb75df66e6868b9af0eee8a7e4b61ef8a459518e)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Qubit_exp.sol) | _

### Insufficient Token Validation
* **[Multichain (Anyswap)](https://twitter.com/MultichainOrg)** | 20220118 | $1.4 million | [[ZenGo](https://medium.com/zengo/without-permit-multichains-exploit-explained-8417e8c1639b)] | [[Transaction](https://etherscan.io/tx/0xe50ed602bd916fc304d53c4fed236698b71691a95774ff0aeeb74b699c6227f7)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Anyswap_poc.t.sol) | _


### Price Manipulation

* **[SellToken](https://twitter.com/TrustTheTrident)** | 20230513 | $197K | [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1657324561577435136)] | [[Transaction](https://bscscan.com/tx/0x7d04e953dad4c880ad72b655a9f56bc5638bf4908213ee9e74360e56fa8d7c6a)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SellToken_exp.sol) | _

* **[Never Fall]()** | 20230503 | $74K | [BeosinAlert](https://twitter.com/BeosinAlert/status/1653619782317662211), [Phalcon_xyz](https://twitter.com/Phalcon_xyz/status/1653604670697521153)] | [[Transaction](https://bscscan.com/tx/0xccf513fa8a8ed762487a0dcfa54aa65c74285de1bc517bd68dbafa2813e4b7cb)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/NeverFall_sol.sol) | _

* **[MonoX Finance](https://twitter.com/MonoXFinance)** | 20211130 | $31 million | [[SlowMist](https://slowmist.medium.com/detailed-analysis-of-the-31-million-monox-protocol-hack-574d8c44a9c8)] | [[Transaction](https://etherscan.io/tx/0x9f14d093a2349de08f02fc0fb018dadb449351d0cdb7d0738ff69cc6fef5f299)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Mono_exp.t.sol) | _

* **[Cream Finance](https://twitter.com/CreamdotFinance)** | 20211027 | $130M | [[Immunefi](https://medium.com/immunefi/hack-analysis-cream-finance-oct-2021-fc222d913fc5)] | [[Transaction](https://etherscan.io/tx/0x0fe2542079644e107cbf13690eb9c2c65963ccb79089ff96bfaf8dced2331c92)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Cream_2_exp.sol) | _

* **[Indexed Finance](https://twitter.com/ndxfi)** | 20211015 | $16M | [[BlockSecTeam](https://blocksecteam.medium.com/the-analysis-of-indexed-finance-security-incident-8a62b9799836)] | [[Transaction](https://etherscan.io/tx/0x44aad3b853866468161735496a5d9cc961ce5aa872924c5d78673076b1cd95aa)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/IndexedFinance_exp.t.sol) | _

### SushiSwap Miso
* **[SushiSwap](https://twitter.com/SushiSwap)** | 20210916 | All funds returned | [[Paradigm](https://www.paradigm.xyz/2021/08/two-rights-might-make-a-wrong)] | [[Transaction](https://etherscan.io/tx/0x78d6355703507f88f2090eb780d245b0ab26bf470eabdb004761cedf3b1cda44)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Sushimiso_exp.sol) | _

### Nimbus Platform
* **[Nimbus Platform](https://twitter.com/nmbplatform)** | 20210915 | 1.45 ETH | _ | [[Transaction](https://etherscan.io/tx/0x5908622ce9670fdcd7954aa098aadb3e13882f198b795c6fea5ee6fc2c802d3c)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Nimbus_exp.sol) | [Twitter](https://twitter.com/BlockSecTeam/status/1438100688215560192)

### NowSwap Platform
* **[NowSwap Platform](https://twitter.com/nowswap_org)** | 20210915 | 158.28 WETH and 535,706 USDT | _ | [[Transaction](https://etherscan.io/tx/0xf3158a7ea59586c5570f5532c22e2582ee9adba2408eabe61622595197c50713)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/NowSwap_exp.sol) | [Twitter](https://twitter.com/BlockSecTeam/status/1438100688215560192)

### Deflationary token incompatible
* **[ZABU Finance](https://twitter.com/zabufinance)** | 20210912 | 200 ETH | [[Slowmist](https://slowmist.medium.com/brief-analysis-of-zabu-finance-being-hacked-44243919ea29)] | [[Transaction](https://snowtrace.io/tx/0x8b3042e55a63f39bb388240a089cf4d51e59abe7cb0bff303c6dbb19eaeb75ac)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/ZABU_exp.sol) | _


### Bridge, getting around modifier through cross-chain message
* **[Poly Network](https://twitter.com/PolyNetwork2)** | 20210811 | $611M | [[Rekt](https://rekt.news/polynetwork-rekt/)] | [[Transaction](https://etherscan.io/tx/0xb1f70464bd95b774c6ce60fc706eb5f9e35cb5f06e6cfe7c17dcda46ffd59581/advanced)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/PolyNetwork/PolyNetwork_exp.sol) | _


### (I) Lost keys and minting (II) Vulnerable emergencyWithdraw
* **[Levyathan Finance](https://twitter.com/)** | 20210728 | $1.5M | [[Medium](https://levyathan-index.medium.com/post-mortem-levyathan-c3ff7f9a6f65)] | [[Transaction](https://bscscan.com/tx/0xfd30def124c1345606598ae4817ae184fc1918fc638111c6e71bc9752361fd87)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Levyathan_poc.sol) | _

### Bridge, logic flaw
* **[Chainswap](https://twitter.com/chain_swap)** | 20210710 | $4.4M | [[Medium](https://chain-swap.medium.com/chainswap-exploit-11-july-2021-post-mortem-6e4e346e5a32)] | [[Transaction](https://bscscan.com/tx/0x83b4adaf73ad34c5c53aa9b805579ed74bc1391c5297201e6457cde709dff723)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Chainswap_exp2.sol) | _

* **[Chainswap](https://twitter.com/chain_swap)** | 20210702 | $.8M | [[Medium](https://chain-swap.medium.com/chainswap-post-mortem-and-compensation-plan-90cad50898ab)] | [[Transaction](https://etherscan.io/tx/0x5c5688a9f981a07ed509481352f12f22a4bd7cea46a932c6d6bbe67cca3c54be)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Chainswap_exp1.sol) | _

### Deflationary token uncompatible
* **[SafeDollar](https://twitter.com/safedollarfi)** | 20210628 | $.2M | [[Twitter](https://twitter.com/peckshield/status/1409443556251430918)] | [[Transaction](https://etherscan.io/tx/-)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/SafeDollar_exp.sol) | _

### Doesn’t burn shares
* **[Eleven Finance](https://twitter.com/ElevenFinance)** | 20210622 | $4.6M | [[Medium](https://peckshield.medium.com/eleven-finance-incident-root-cause-analysis-123b5675fa76)] | [[Transaction](https://bscscan.com/tx/0xeaaa8f4d33b1035a790f0d7c4eb6e38db7d6d3b580e0bbc9ba39a9d6b80dd250)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Eleven.sol) | _


### Mathematical flaw + Reentrancy
* **[BurgerSwap](https://twitter.com/burger_swap)** | 20210527 | $7.2M | [[Tweet](https://twitter.com/Mudit__Gupta/status/1398156036574306304)] | [[Contract](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BurgerSwap_exp.sol)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BurgerSwap_exp.sol) | _

### Incorrect calculation

* **[SNOOD](https://twitter.com/SchnoodleDAO)** | 20220618 | 104 ETH | [[ethereum.stackexchange](https://ethereum.stackexchange.com/questions/130472/attack-on-erc-777-smart-contract-and-uniswapv2pair-resulting-in-104-eth-liquidit), [ethtx.info](https://ethtx.info/mainnet/0x9a6227ef97d7ce75732645bd604ef128bb5dfbc1bfbe0966ad1cd2870d45a20e/)] | [Transaction](https://etherscan.io/tx/0x9a6227ef97d7ce75732645bd604ef128bb5dfbc1bfbe0966ad1cd2870d45a20e) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Snood_poc.t.sol) | _function _spendAllowance_

* **[PancakeHunny](https://hunny.finance/#/pools)** | 20210603 | 216 BNB | [[Medium](https://medium.com/hunnyfinance/pancakehunny-post-mortem-analysis-de78967401d8)] | [[Transaction](https://bscscan.com/tx/0x765de8357994a206bb90af57dcf427f48a2021f2f28ca81f2c00bc3b9842be8e)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/PancakeHunny_exp.sol) | _


* **[Uranium](https://twitter.com/UraniumFinance)** | 20210428 | $50M | [[Tweet](https://twitter.com/FrankResearcher/status/1387347025742557186)] | [[Transaction](https://bscscan.com/tx/0x5a504fe72ef7fc76dfeb4d979e533af4e23fe37e90b5516186d5787893c37991)] ｜[POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/Uranium_exp.sol) | _


### Wrong balance check
* **FAPEN** | 20230529 | $600 | [[hexagate_](https://twitter.com/hexagate_/status/1663501550600302601)] | [Transaction](https://bscscan.com/tx/0xa2be65e439eb182e8f2acfe7eff9a4bab55eb3cd789dcc0ddd19bf811af78a93) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/FAPEN_exp.sol) | _

### Wrong visibility in function
* **NOON** | 20230529 | $2K | [[hexagate_](https://twitter.com/hexagate_/status/1663501545105702912)] | [Transaction](https://etherscan.io/tx/0x23fb7f093e827ed061aafb574cfd420eab879621c7f78cb341292e106a3a88c0) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/NOON_exp.sol) | _


### Fee Machenism Exploitation
* **GPT Token** | 20230525 | $42K | [[Phalcon_xyz](https://twitter.com/Phalcon_xyz/status/1661424685320634368)] | [Transaction](https://bscscan.com/tx/0xb77cb34cd01204bdad930d8c172af12462eef58dea16199185b77147d6533391) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/GPT_exp.sol) | _skim_

### wrong implemention
* **[DEI](https://twitter.com/cmichelio/status/1646422861219807233)** | 20230505 | $5.4M | [[eugenioclrc](https://twitter.com/eugenioclrc/status/1654576296507088906)] | [Transaction](https://arbiscan.io/tx/0xb1141785b7b94eb37c39c37f0272744c6e79ca1517529fec3f4af59d4c3c37ef) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/DEI_exp.sol) | _

### Lack Slippage Protection
* **[BabyDogeCoin02](https://twitter.com/BabyDogeCoin)** | 20230621 | $441BNB | [[hexagate_](https://twitter.com/hexagate_/status/1671517819840745475)] | [Transaction](https://bscscan.com/tx/0xbaf3e4841614eca5480c63662b41cd058ee5c85dc69198b29e7ab63b84bc866c) | [POC](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/BabyDogeCoin02_exp.sol) | _

## notes:
* In most cases, `Flashloan` are not the root cause of attacks; they are merely a lending method. If an attack cannot be executed `without` the step of a Flashloan, only then it can been classified as a `Flashloan attack`.
