# StringInStr
     $oColItems = $oWMIService.ExecQuery('Select * From Win32_DiskDrive Where DeviceID="' &amp; $aReturn[4] &amp; '"', 'WQL', 0x30)     If IsObj($oColItems) Then         For $oObjectItem In $oColItems             $aReturn[5] = $oObjectItem.PNPDeviceID ; PNPDeviceID value.         Next     EndIf     $aArray = $aReturn     Return StringInStr($aReturn[5], 'SSD') > 0 EndFunc   ;==>_IsDriveSS
