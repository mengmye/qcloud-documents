云点播 API 于**北京时间2021年5月1日**全面升级至3.0版本。基于2.0版本接口访问时延较高和使用复杂的考虑，原云点播 VOD 的 API 2.0 接口服务将不再提供技术支持，并将于**北京时间2022年11月30日**下线。如果您的业务还在使用云点播 VOD 的 API 2.0 相关接口，建议尽快将服务升级至云点播 API 3.0 接口，以免对您的业务造成影响。具体详情可参见 [《迁移指引》](https://doc.weixin.qq.com/doc/w3_AJ4ATAbdAFwo8dQuatDQf0mkSZsNu?scode=AJEAIQdfAAoccCXydAAJ4ATAbdAFw&version=4.0.12.6015&platform=win)。

## 服务端 API 使用
云点播服务端 API 的具体使用方法和 [腾讯云 API][云 API] 相同。为了方便用户调用 API，云点播提供了 [服务端 API SDK][SDK] 供开发者使用。

#### 请求结构
* [请求结构简介](https://cloud.tencent.com/document/api/213/6975)
* [公共请求参数](https://cloud.tencent.com/document/api/213/6976)
* [接口请求参数](https://cloud.tencent.com/document/api/213/6977)
* [最终请求形式](https://cloud.tencent.com/document/api/213/6978)

<!---#### 签名方法
* [签名方法](https://cloud.tencent.com/document/api/213/6984)--->

#### 返回结果
* [正确返回结果](https://cloud.tencent.com/document/api/213/6980)
* [错误返回结果](https://cloud.tencent.com/document/api/213/6981)
* [公共错误码][公共错误码]

#### 云点播业务错误码
除了 [云 API][云 API] [公共错误码][公共错误码]，云点播还有自己的专有错误码：

| 错误码 | 含义说明|
|---------|---------|
|-43001 | 查询，查询命令执行：解码失败， ffmpeg 通知文件已损坏|
|-43029 | 查询，查询命令执行：解码失败，ffmpeg 解码失败|
|-43089 | 查询，查询命令执行：元信息缺失，原视频编解码器未知|
|-43090 | 查询，查询命令执行：元信息缺失，原视频音频帧大小未知|
|-43091 | 查询，查询命令执行：元信息缺失，原视频音频帧格式未知|
|-43092 | 查询，查询命令执行：元信息缺失，原视频音频帧率未知|
|-43093 | 查询，查询命令执行：元信息缺失，原视频音频通道数未知|
|-43094 | 查询，查询命令执行：元信息缺失，no decodable DTS frames|
|-43095 | 查询，查询命令执行：元信息缺失，原视频视频宽高未知|
|-43096 | 查询，查询命令执行：元信息缺失，原视频色度空间未知|
|-43097 | 查询，查询命令执行：元信息缺失，no frame in rv30,40 and no sar|
|-43098 | 查询，查询命令执行：End of file|
|-43099 | 查询，查询命令执行：seeking outside actual filesize|
|-43101 | 查询，查询待拼接文件的命令执行：解码失败， ffmpeg 通知文件已损坏|
|-43129 | 查询，查询待拼接文件的命令执行：解码失败， ffmpeg 解码失败|
|-43189 | 查询，查询待拼接文件的命令执行：元信息缺失， 原视频编解码器未知|
|-43190 | 查询，查询待拼接文件的命令执行：元信息缺失， 原视频音频帧大小未知|
|-43191 | 查询，查询待拼接文件的命令执行：元信息缺失， 原视频音频帧格式未知|
|-43192 | 查询，查询待拼接文件的命令执行：元信息缺失， 原视频音频帧率未知|
|-43193 | 查询，查询待拼接文件的命令执行：元信息缺失， 原视频音频通道数未知|
|-43194 | 查询，查询待拼接文件的命令执行：元信息缺失， no decodable DTS frames|
|-43195 | 查询，查询待拼接文件的命令执行：元信息缺失， 原视频视频宽高未知|
|-43196 | 查询，查询待拼接文件的命令执行：元信息缺失， 原视频色度空间未知|
|-43197 | 查询，查询待拼接文件的命令执行：元信息缺失， no frame in rv30,40 and no sar|
|-43198 | 查询，查询待拼接文件的命令执行：End of file|
|-43199 | 查询，查询待拼接文件的命令执行：seeking outside actual filesize|
|-44001 | 截图，截图命令执行：解码失败，ffmpeg 通知文件已损坏|
|-44029 | 截图，截图命令执行：解码失败，ffmpeg 解码失败|
|-44089 | 截图，截图命令执行：元信息缺失，原视频编解码器未知|
|-44090 | 截图，截图命令执行：元信息缺失，原视频音频帧大小未知|
|-44091 | 截图，截图命令执行：元信息缺失，原视频音频帧格式未知|
|-44092 | 截图，截图命令执行：元信息缺失，原视频音频帧率未知|
|-44093 | 截图，截图命令执行：元信息缺失，原视频音频通道数未知|
|-44094 | 截图，截图命令执行：元信息缺失，no decodable DTS frames|
|-44095 | 截图，截图命令执行：元信息缺失，原视频视频宽高未知|
|-44096 | 截图，截图命令执行：元信息缺失，原视频色度空间未知|
|-44097 | 截图，截图命令执行：元信息缺失， no frame in rv30,40 and no sar|
|-44098 | 截图，截图命令执行：End of file|
|-44099 | 截图，截图命令执行：seeking outside actual filesize|
|-44101 | 截图，获取截图信息命令执行：解码失败，ffmpeg 通知文件已损坏|
|-44129 | 截图，获取截图信息命令执行：解码失败，ffmpeg 解码失败|
|-44189 | 截图，获取截图信息命令执行：元信息缺失，原视频编解码器未知|
|-44190 | 截图，获取截图信息命令执行：元信息缺失，原视频音频帧大小未知|
|-44191 | 截图，获取截图信息命令执行：元信息缺失，原视频音频帧格式未知|
|-44192 | 截图，获取截图信息命令执行：元信息缺失，原视频音频帧率未知|
|-44193 | 截图，获取截图信息命令执行：元信息缺失，原视频音频通道数未知|
|-44194 | 截图，获取截图信息命令执行：元信息缺失，no decodable DTS frames|
|-44195 | 截图，获取截图信息命令执行：元信息缺失，原视频视频宽高未知|
|-44196 | 截图，获取截图信息命令执行：元信息缺失，原视频色度空间未知|
|-44197 | 截图，获取截图信息命令执行：元信息缺失，no frame in rv30,40 and no sar|
|-44198 | 截图，获取截图信息命令执行：End of file|
|-44199 | 截图，获取截图信息命令执行：seeking outside actual filesize|
|-45001 | 音视频转码，转码命令执行：解码失败，ffmpeg 通知文件已损坏|
|-45029 | 音视频转码，转码命令执行：解码失败，ffmpeg 解码失败|
|-45089 | 音视频转码，转码命令执行：元信息缺失，原视频编解码器未知|
|-45090 | 音视频转码，转码命令执行：元信息缺失，原视频音频帧大小未知|
|-45091 | 音视频转码，转码命令执行：元信息缺失，原视频音频帧格式未知|
|-45092 | 音视频转码，转码命令执行：元信息缺失，原视频音频帧率未知|
|-45093 | 音视频转码，转码命令执行：元信息缺失，原视频音频通道数未知|
|-45094 | 音视频转码，转码命令执行：元信息缺失，no decodable DTS frames|
|-45095 | 音视频转码，转码命令执行：元信息缺失，原视频视频宽高未知|
|-45096 | 音视频转码，转码命令执行：元信息缺失，原视频色度空间未知|
|-45097 | 音视频转码，转码命令执行：元信息缺失，no frame in rv30,40 and no sar|
|-45098 | 音视频转码，转码命令执行：End of file|
|-45099 | 音视频转码，转码命令执行：seeking outside actual filesize|
|-45101 | 音视频转码，校验转码后文件前获取文件信息：解码失败，ffmpeg 通知文件已损坏|
|-45129 | 音视频转码，校验转码后文件前获取文件信息：解码失败，ffmpeg 解码失败|
|-45189 | 音视频转码，校验转码后文件前获取文件信息：元信息缺失，原视频编解码器未知|
|-45190 | 音视频转码，校验转码后文件前获取文件信息：元信息缺失，原视频音频帧大小未知|
|-45191 | 音视频转码，校验转码后文件前获取文件信息：元信息缺失，原视频音频帧格式未知|
|-45192 | 音视频转码，校验转码后文件前获取文件信息：元信息缺失，原视频音频帧率未知|
|-45193 | 音视频转码，校验转码后文件前获取文件信息：元信息缺失，原视频音频通道数未知|
|-45194 | 音视频转码，校验转码后文件前获取文件信息：元信息缺失，no decodable DTS frames|
|-45195 | 音视频转码，校验转码后文件前获取文件信息：元信息缺失，原视频视频宽高未知|
|-45196 | 音视频转码，校验转码后文件前获取文件信息：元信息缺失，原视频色度空间未知|
|-45197 | 音视频转码，校验转码后文件前获取文件信息：元信息缺失，no frame in rv30,40 and no sar|
|-45198 | 音视频转码，校验转码后文件前获取文件信息：End of file|
|-45199 | 音视频转码，校验转码后文件前获取文件信息：seeking outside actual filesize|
|-45201 | 音视频转码，上传文件前获取文件信息：解码失败，ffmpeg 通知文件已损坏|
|-45229 | 音视频转码，上传文件前获取文件信息：解码失败，ffmpeg 解码失败|
|-45289 | 音视频转码，上传文件前获取文件信息：元信息缺失，原视频编解码器未知|
|-45290 | 音视频转码，上传文件前获取文件信息：元信息缺失，原视频音频帧大小未知|
|-45291 | 音视频转码，上传文件前获取文件信息：元信息缺失，原视频音频帧格式未知|
|-45292 | 音视频转码，上传文件前获取文件信息：元信息缺失，原视频音频帧率未知|
|-45293 | 音视频转码，上传文件前获取文件信息：元信息缺失，原视频音频通道数未知|
|-45294 | 音视频转码，上传文件前获取文件信息：元信息缺失，no decodable DTS frames|
|-45295 | 音视频转码，上传文件前获取文件信息：元信息缺失，原视频视频宽高未知|
|-45296 | 音视频转码，上传文件前获取文件信息：元信息缺失，原视频色度空间未知|
|-45297 | 音视频转码，上传文件前获取文件信息：元信息缺失，no frame in rv30,40 and no sar|
|-45298 | 音视频转码，上传文件前获取文件信息：End of file|
|-45299 | 音视频转码，上传文件前获取文件信息：seeking outside actual filesize|
|-47100 | 原文件不符合要求，源文件信息格式非 JSON|
|-47101 | 原文件不符合要求，源信息缺少宽、高 或色度空间的原信息|
|-47102 | 原文件不符合要求，源信息未知编码器|
|-47104 | 原文件不符合要求，源信息时长不合法(<0.01 or >604800)|
|-47200 | 原文件不符合要求，文件的时长信息为0|
|-47300 | 原文件不符合要求，拼接超过最大值限制|
|-47301 | 原文件不符合要求，拼接文件分辨率不一致|
|-47302 | 原文件不符合要求，拼接获取视频文件源信息失败|
|-47400 | 原文件不符合要求，视频文件的音频和视频不存在|
|-47401 | 原文件不符合要求，转音频任务，原文件无音频数据|
|-47402 | 原文件不符合要求，转视频任务，原文件无视频数据|
|-47403 | 原文件不符合要求，视频文件 width/high/rotate/dar_w/dar_h 不合法|
|-49101 | 音视频转码，校验转码后文件：解码失败，ffmpeg 通知文件已损坏|
|-49129 | 音视频转码，校验转码后文件：解码失败，ffmpeg 解码失败|
|-49189 | 音视频转码，校验转码后文件：元信息缺失，原视频编解码器未知|
|-49190 | 音视频转码，校验转码后文件：元信息缺失，原视频音频帧大小未知|
|-49191 | 音视频转码，校验转码后文件：元信息缺失，原视频音频帧格式未知|
|-49192 | 音视频转码，校验转码后文件：元信息缺失，原视频音频帧率未知|
|-49193 | 音视频转码，校验转码后文件：元信息缺失，原视频音频通道数未知|
|-49194 | 音视频转码，校验转码后文件：元信息缺失，no decodable DTS frames|
|-49195 | 音视频转码，校验转码后文件：元信息缺失，原视频视频宽高未知|
|-49196 | 音视频转码，校验转码后文件：元信息缺失，原视频色度空间未知|
|-49197 | 音视频转码，校验转码后文件：元信息缺失，no frame in rv30,40 and no sar|
|-49198 | 音视频转码，校验转码后文件：End of file|
|-49199 | 音视频转码，校验转码后文件：seeking outside actual filesize|

[云 API]: https://cloud.tencent.com/product/api "云 API"
[公共错误码]: https://cloud.tencent.com/document/api/213/10146 "公共错误码"
[SDK]: https://cloud.tencent.com/document/developer-resource "SDK"




