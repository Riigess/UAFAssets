
# UAFAssets
This is an effort to track UAF assets going through https://gdmf.apple.com/v2/assets

# Protocol
gdmf.apple.com uses [JSON Web Tokens](https://jwt.io) to communicate. Sending a simple request to https://gdmf.apple.com/v2/assets might look a little something like this;
```
{
    "AssetAudience": "02d8e57e-dd1c-4090-aa50-b4ed2aef0062",
    "AssetType": "com.apple.MobileAsset.UAF.FM.GenerativeModels",
    "ClientVersion": 2,
    "CertIssuanceDay": "2023-12-10",
    "DeviceName": "Mac",
    "TrainName": "GlowSeed"
}
```
The AssetAudience value passed is a generic AssetAudience for macOS. This can be any Mac-specific AssetAudience and Pallas will return an audience for us to use when requesting assets later.

The AssetType can be changed, but should always start with "com.apple.MobileAsset.UAF" unless another asset is discovered to not follow this pattern in `/System/Library/AssetsV2`.

The DeviceName and TrainName fields should go in pairs. Mac/SunburstSeed, Mac/GlowSeed, iPhone/DawnSeed, iPhone/CrystalSeed, "Apple Vision"/BorealisSeed, "Apple Vision"/ConstellationSeed, etc.


# Special Thanks
A few people that helped lead to the tracking effort. Their past research wouldn't have made this possible...besides Nicolas was looking to remove these assets from their repo anyways lol.
- [@Nicolás17](https://github.com/nicolas17)
- [@r00tfs](https://github.com/R00tFS)
- [@dhinakg](https://github.com/dhinakg)

And the salty person on the internet who called me an AI ~ [@Siguza](https://github.com/Siguza)
