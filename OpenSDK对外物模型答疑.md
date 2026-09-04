# OpenSDK对外物模型答疑

## 休眠时间段设置

请求：`/api-cn-test.superacme.com/operation/api/v1/unified/operation/down`

入参

*   deviceId:   设备id
    
*   method:   thing.service.property.set
    
*   params:   "\[{\"days\":\[{\"DayOfWeek\":0,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":1,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":2,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":3,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":4,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":5,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":6,\"BeginTime\":57600,\"EndTime\":61200}\]},{\"days\":\[{\"DayOfWeek\":0,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":1,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":2,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":3,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":4,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":5,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":6,\"BeginTime\":0,\"EndTime\":3600}\]}\]"   //DayOfWeek是从0-6，分别表示周日到周六，BeginTime表示开始时间，EndTime表示结束时间，返回是从0-86399，86399表示当天的23点59分59秒
    
*   identifier:   SleepTimeConfig
    
*   id:   请求   ID
    

```json
{
    "deviceId": "123123123123",
    "method": "thing.service.property.set",
    "params": "[{\"days\":[{\"DayOfWeek\":0,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":1,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":2,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":3,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":4,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":5,\"BeginTime\":57600,\"EndTime\":61200},{\"DayOfWeek\":6,\"BeginTime\":57600,\"EndTime\":61200}]},{\"days\":[{\"DayOfWeek\":0,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":1,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":2,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":3,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":4,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":5,\"BeginTime\":0,\"EndTime\":3600},{\"DayOfWeek\":6,\"BeginTime\":0,\"EndTime\":3600}]}]",
    "identifier": "SleepTimeConfig",
    "id": "c3efda44-b82a-44e9-b016-2885eda784df"
}
```

出参

*   code：0表示成功，非0表示失败。同success，2者判断其中一个就好
    
*   data:   {}   默认返回空
    
*   message：服务端返回的提示
    
*   success：true/false
    

```json
{
	"code": 0,
	"data": {},
	"message": "成功",
	"success": true
}
```

## 格式化SD卡

请求：`/api-cn-test.superacme.com/operation/api/v1/unified/operation/down`

入参

*   productKey:   设备   productKey
    
*   deviceName:   设备   deviceName
    
*   method:   thing.service.FormatStorageMediumV2
    
*   params:   {}
    
*   identifier:   FormatStorageMediumV2
    
*   id:   请求   ID
    

```json
{
	"productKey": "PsVm8h030jpe",
	"deviceName": "550001000098000001234",
	"method": "thing.service.FormatStorageMediumV2",
	"params": {},
	"identifier": "FormatStorageMediumV2",
	"id": "c3efda44-b82a-44e9-b016-2885eda784df"
}
```

出参

*   code：0表示成功，非0表示失败。同success，2者判断其中一个就好
    
*   data:   
    
    *   success（0：格式化失败、1：成功、2：视频回放中，无法格式化、3：视频录制中，无法格式化）
        
*   message：服务端返回的提示
    
*   success：true/false
    

```json
{
	"code": 0,
	"data": {
		"success": 1
	},
	"message": "成功",
	"success": true
}
```