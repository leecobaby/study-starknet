# 学习 straknet

1. 项目介绍

   本仓库是根据 WTF 学院课程，使用 `protostar` 创建的学习仓库
   https://starknet.wtf.academy/docs/Tool/

2. 部署工作

   部署账户 只需一次
   protostar calculate-account-address --account-class-hash 0x025ec026985a3bf9d0cc1fe17326b245dfdc3ff89b8fde106542a3ea56c5a918 --account-address-salt 1

   申明合约 (合约内容必须和链上不一，否则生产的哈希会和链上一样，导致这步报错)
   protostar declare hello_starknet --account-address 0x07623f7d24c9cead012d41d7ba144a019ab46f4cb600c6b504ca3a7d82994e1c --max-fee auto --network testnet

   部署合约
   protostar deploy 0x0109b62222039c3d6fe28c0c6501b34577ebeca0b375537d397fab3c33389974 --network testnet --max-fee auto --account-address 0x07623f7d24c9cead012d41d7ba144a019ab46f4cb600c6b504ca3a7d82994e1c
