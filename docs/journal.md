# JOURNAL

---------------------------------------------------------------------
## 2021/01/15 (FR)













---------------------------------------------------------------------
## 2021/01/14 (TH)

Table 2-6 Extended Fields of the Payload Header 

Presentation Time Stamp (PTS). 
The source clock time in native device clock units when the raw frame capture 
begins. This field may be repeated for 
multiple payload transfers comprising a 
single video frame, with the restriction 
that the value shall remain the same 
throughout that video frame. The PTS is 
in the same units as specified in the 
dwClockFrequency field of the Video 
Probe Control response.



static uint32_t uvc_timer_to_pts(uint32_t timer)
{
	uint32_t us;
	uint32_t pts;
	us = timer / 150;
	pts = us * 100000;
	return pts;
}

void uvc_bulk_in_hdmi(void)

CX3 - Utilizing the UVC PTS (Presentation Time Stamp) field
https://community.cypress.com/t5/USB-Superspeed-Peripherals/CX3-Utilizing-the-UVC-PTS-Presentation-Time-Stamp-field/td-p/139889

https://community.cypress.com/t5/USB-Superspeed-Peripherals/CX3-timestamp/td-p/103127


DE
http://www.xwinman.org/

Developing Microsoft Media Foundation Applications

Understanding Open Source and Free Software Licensing: Guide to Navigating Licensing Issues in Existing & New Software 1st Edition, Kindle Edition
by Andrew M. St. Laurent 

Intellectual Property and Open Source: A Practical Guide to Protecting Code 1st Edition, Kindle Edition
by Van Lindberg 

How Open Source Ate Software: Understand the Open Source Movement and So Much More 1st ed. Edition, Kindle Edition
by Gordon Haff

Producing Open Source Software: How to Run a Successful Free Software Project Kindle Edition
by Karl Fogel



[2021-01-14 17:19:03.439] [avm_setup_is_done] val=0
[2021-01-14 17:19:06.122] [avm_setup_is_done] val=1




[2021-01-14 17:29:56.725] Qoo vic 5 16 Video State : Check HDMI->Update Video
[2021-01-14 17:29:56.935] fusb300_vbus_change : FUSB300_OFFSET_GCR : 0x0
[2021-01-14 17:29:56.935] [avm_setup_is_done] val=0
...
[2021-01-14 17:29:59.827] avm_ext_dev_state_send@385 1920x540,interlace,@fps:60
[2021-01-14 17:29:59.903] fusb300_ep0
[2021-01-14 17:29:59.903]   clear_feature
[2021-01-14 17:29:59.903] Clear Feature : U2_ENABLE
[2021-01-14 17:29:59.903] [avm_setup_is_done] val=1
[2021-01-14 17:29:59.903] fusb300_ep0
[2021-01-14 17:29:59.903]   set_interface
[2021-01-14 17:29:59.903] Audio HDMI State : ->Prepare Start
[2021-01-14 17:29:59.903] enable EP1 INT
[2021-01-14 17:29:59.903] uvc_main_audio_hdmi_in uvc_iso_in_HDMI_Status=1,uvc_iso_out_DAC_Status=0
[2021-01-14 17:29:59.903] Audio HDMI State : Prepare->Check HDMI
[2021-01-14 17:29:59.952] ---------------------------------------
[2021-01-14 17:29:59.952] GPIO2 = 0(2676)
[2021-01-14 17:29:59.952] ---------------------------------------
[2021-01-14 17:29:59.952] Audio HDMI State : Check HDMI->Stable


[2021-01-14 17:19:02.942] Qoo vic 4 16 Video State : Check HDMI->Update Video
[2021-01-14 17:19:03.439] fusb300_vbus_change : FUSB300_OFFSET_GCR : 0x0
[2021-01-14 17:19:03.439] [avm_setup_is_done] val=0
...
[2021-01-14 17:19:05.809] avm_ext_dev_state_send@385 1280x720,progressive,@fps:60
[2021-01-14 17:19:06.122] fusb300_ep0
[2021-01-14 17:19:06.122]   clear_feature
[2021-01-14 17:19:06.122] Clear Feature : U2_ENABLE
[2021-01-14 17:19:06.122] [avm_setup_is_done] val=1
[2021-01-14 17:19:06.122] fusb300_cmdend
[2021-01-14 17:19:06.122] fusb300_ep0
[2021-01-14 17:19:06.122]   set_interface
[2021-01-14 17:19:06.122] Audio HDMI State : ->Prepare Start
[2021-01-14 17:19:06.122] enable EP1 INT
[2021-01-14 17:19:06.122] uvc_main_audio_hdmi_in uvc_iso_in_HDMI_Status=1,uvc_iso_out_DAC_Status=0
[2021-01-14 17:19:06.122] Audio HDMI State : Prepare->Check HDMI
[2021-01-14 17:19:06.171] ---------------------------------------
[2021-01-14 17:19:06.171] GPIO2 = 0(2676)
[2021-01-14 17:19:06.171] ---------------------------------------
[2021-01-14 17:19:06.171] Audio HDMI State : Check HDMI->Stable

[2021-01-14 17:20:28.493] Qoo vic 16 5 Video State : Check HDMI->Update Video
[2021-01-14 17:20:28.648] fusb300_vbus_change : FUSB300_OFFSET_GCR : 0x0
[2021-01-14 17:20:28.994] [avm_setup_is_done] val=0
...
[2021-01-14 17:20:31.311] avm_ext_dev_state_send@385 1920x1080,progressive,@fps:60
[2021-01-14 17:20:31.678] fusb300_ep0
[2021-01-14 17:20:31.678]   clear_feature
[2021-01-14 17:20:31.678] Clear Feature : U2_ENABLE
[2021-01-14 17:20:31.678] [avm_setup_is_done] val=1
[2021-01-14 17:20:31.678] fusb300_ep0
[2021-01-14 17:20:31.678]   set_interface
[2021-01-14 17:20:31.678] Audio HDMI State : ->Prepare Start
[2021-01-14 17:20:31.678] enable EP1 INT
[2021-01-14 17:20:31.678] uvc_main_audio_hdmi_in uvc_iso_in_HDMI_Status=1,uvc_iso_out_DAC_Status=0
[2021-01-14 17:20:31.678] Audio HDMI State : Prepare->Check HDMI
[2021-01-14 17:20:31.726] ---------------------------------------
[2021-01-14 17:20:31.726] GPIO2 = 0(2676)
[2021-01-14 17:20:31.726] ---------------------------------------
[2021-01-14 17:20:31.726] Audio HDMI State : Check HDMI->Stable

[2021-01-14 17:19:43.745] Qoo vic 5 4 Video State : Check HDMI->Update Video
[2021-01-14 17:19:43.956] fusb300_vbus_change : FUSB300_OFFSET_GCR : 0x0
[2021-01-14 17:19:43.956] [avm_setup_is_done] val=0
...
[2021-01-14 17:19:46.809] avm_ext_dev_state_send@385 1920x540,interlace,@fps:60
[2021-01-14 17:19:46.929] fusb300_ep0
[2021-01-14 17:19:46.929]   clear_feature
[2021-01-14 17:19:46.929] Clear Feature : U2_ENABLE
[2021-01-14 17:19:46.929] [avm_setup_is_done] val=1
[2021-01-14 17:19:46.929] fusb300_ep0
[2021-01-14 17:19:46.929]   set_interface
[2021-01-14 17:19:46.929] Audio HDMI State : ->Prepare Start
[2021-01-14 17:19:46.929] enable EP1 INT
[2021-01-14 17:19:46.929] uvc_main_audio_hdmi_in uvc_iso_in_HDMI_Status=1,uvc_iso_out_DAC_Status=0
[2021-01-14 17:19:46.929] Audio HDMI State : Prepare->Check HDMI
[2021-01-14 17:19:46.978] ---------------------------------------
[2021-01-14 17:19:46.978] GPIO2 = 0(2676)
[2021-01-14 17:19:46.978] ---------------------------------------
[2021-01-14 17:19:46.978] Audio HDMI State : Check HDMI->Stable


[2021-01-14 17:57:32.632] Qoo vic 16 5 Video State : Check HDMI->Update Video
[2021-01-14 17:57:32.767] fusb300_vbus_change : FUSB300_OFFSET_GCR : 0x0
[2021-01-14 17:57:32.815] [avm_setup_is_done] val=0

[2021-01-14 17:57:35.739] Clear Feature : U2_ENABLE
[2021-01-14 17:57:35.739] [avm_setup_is_done] val=1





[2021-01-14 17:59:28.046] Qoo vic 5 16 Video State : Check HDMI->Update Video
[2021-01-14 17:59:28.248] fusb300_vbus_change : FUSB300_OFFSET_GCR : 0x0
[2021-01-14 17:59:28.248] [avm_setup_is_done] val=0

[2021-01-14 17:59:31.286] fusb300_ep0
[2021-01-14 17:59:31.323]   clear_feature
[2021-01-14 17:59:31.323] Clear Feature : U2_ENABLE
[2021-01-14 17:59:31.323] [avm_setup_is_done] val=1


---------------------------------------------------------------------
## 2021/01/13 (WE)

回家反省自己，怎麼連個BU113裝置的名稱字串都搞不定。覺得自己應該去讀SPEC，不應該問你、把你的回覆當標準。
這問題挺有意思的，好幾位同事寫了好幾個相同的產品名稱問題，後來都關掉了。沒有人真的去讀規格書、跟規格書比對。
歹勢啦，昨天講話大聲了些。如果您覺得不舒服，鄭重跟您道歉。

BU113-133
https://www.cypress.com/comment/286026
ithTimerGetCounter(0);


---------------------------------------------------------------------
## 2021/01/12 (TU)

精準閱讀 伊藤真
世界記憶力冠軍的高效記憶筆記  君特‧卡斯騰 Gunther Karsten


109, 115, 102


AP Version:RECetnral v4.6.0.16
FW Vision:0.0.0.7
OS Version:Windows 10 Pro 版本2004 
Platform:Asus X370 Pro

121	13:47:55.320,898
241	13:47:56.321,051

1.001

---------------------------------------------------------------------
## 2021/01/11 (MO)



BU113產生的frames，有timestamp相同的現象，會造成RECentral錄影問題

LAV Filters - Open-Source DirectShow Media Splitter and Decoders [git](https://github.com/Nevcairiel/LAVFilters.git)

16.6666666
16.68335

145 17:12:29.112,003
 25 17:12:28.112,011

1580	17:48:55.884,034
1700	17:48:56.868,881
0.984847

1600	17:48:56.034713
1720	17.48:57.035566
1.001

1500	17:48:55.200590
1620	17:48:56.201645
1.0011

1440	17:48:54.699957
1560	17:48:55.701074
1.0011

1440	19:32:52.874516
1560	19:32:53.874566
1.000
---------------------------------------------------------------------

## 2021/01/09 (SA)

HDR
GC553
 87 1 1A 0 2 0 98 3A 30 75 4C 1D B8 B 0 7D 74 40 13 3D 42 40 0 0 0 0 FF 0 7F 0 0

BU113
 87 1 1A 0 38 2 0 98 3A 30 75 4C 1D B8 B 0 7D 74 40 13 3D 42 40 0 0 0 0 FF 0 7F 0
           --
 87 1 1A 0 2 0 98 3A 30 75 4C 1D B8 B 0 7D 74 40 13 3D 42 40 0 0 0 0 FF 0 7F 0 0
 
 project/HDMI_Bridge/fusb300/usb_flash.c | 18 +++++++++++++----
 project/libavt/avm_config.h             | 12 +++++++++++
 project/libavt/avm_spi_flash.c          | 17 ++++++++++++++++
 project/libavt/avm_spi_flash.h          |  9 ++++++---
 project/libavt/avm_uvc_req.c            | 35 ++++++++++++++++++++++++++-------
 project/libavt/avm_version.c            |  3 +++
 6 files changed, 80 insertions(+), 14 deletions(-)

diff --git a/project/HDMI_Bridge/fusb300/usb_flash.c b/project/HDMI_Bridge/fusb300/usb_flash.c
index ae832f5..91fa545 100644
--- a/project/HDMI_Bridge/fusb300/usb_flash.c
+++ b/project/HDMI_Bridge/fusb300/usb_flash.c
@@ -8,6 +8,7 @@
 #include "../../bootloader/config.h"
 #ifdef AVT_BU113
 #include "avt_gpio.h"
+#include "avm_config.h"
 #endif
 
 
@@ -437,21 +438,30 @@ uint32_t PrepareCustomerAreaData()
 	g_fd = -1;
 
 #ifdef AVT_BU113
-/* debug
+#if 0 /* debug */
 	int cnt = 0;
 	for (int i = 0; i < 32; ++i)
 	{
 		printf("%02x ", *(uint8_t *)(DDRBuf_ptr + CFG_USB_DESCRIPTOR_OFFSET + CFG_USB_DESCRIPTOR_SN_OFFSET + i));
 		if (0 == ((++cnt) % 16)) printf("\n");
 	}
-*/
+#endif
+	unsigned char buf[65536];
+//	memset(buf, 0xFF, SPI_FLASH_BLOCK_SZ);
+	avm_customer_usage_block_read(buf);
+
+	/* byte 13 */
+	g_avm_config.is_hdcp_handshake = buf[13] & 0x1;
+	printf("> %sable HDCP handshake\n", g_avm_config.is_hdcp_handshake ? "En" : "Dis");
+
+	/* byte 0..12 */
 	unsigned char serialnum[13] = {0};
-	avm_usb_sn_get(serialnum, 13);
+	memcpy(serialnum, buf, 13);
 
 	for (int i = 0; i < 13; ++i)
 		if ((serialnum[i] < 0x30) || (serialnum[i] > 0x39)) return ret;
 
-	printf("Serial Number: ");
+	printf("> Serial Number: ");
 	for (int i = 1; i < 14; ++i)
 	{
 		*(uint8_t *)(DDRBuf_ptr + CFG_USB_DESCRIPTOR_OFFSET + CFG_USB_DESCRIPTOR_SN_OFFSET + 2 * i) = serialnum[i - 1];
diff --git a/project/libavt/avm_config.h b/project/libavt/avm_config.h
new file mode 100644
index 0000000..69f5fe3
--- /dev/null
+++ b/project/libavt/avm_config.h
@@ -0,0 +1,12 @@
+#ifndef _AVM_CONFIG_H_
+#define _AVM_CONFIG_H_
+
+typedef struct {
+    
+    unsigned char is_hdcp_handshake;
+
+} avm_config_t;
+
+extern avm_config_t g_avm_config;
+
+#endif /* _AVM_CONFIG_H_ */
diff --git a/project/libavt/avm_spi_flash.c b/project/libavt/avm_spi_flash.c
index 32d99ee..934db40 100644
--- a/project/libavt/avm_spi_flash.c
+++ b/project/libavt/avm_spi_flash.c
@@ -941,6 +941,23 @@ void avm_usb_sn_set(unsigned char* pdata,unsigned short size)
 	avm_customer_usage_block_write(buf);
 }
 
+void avm_customer_usage_block_set_byte(unsigned char *pdata, unsigned offset, unsigned size)
+{
+	unsigned char buf[SPI_FLASH_BLOCK_SZ];
+
+	avm_customer_usage_block_read(buf);
+	memcpy(buf + offset, pdata, size);
+	avm_customer_usage_block_write(buf);
+
+#if 1 /* debug */
+	{
+		avm_customer_usage_block_read(buf);
+		for (int i = 0; i < 16; ++i) printf("%02x ", buf[i]);
+		printf("\n");
+	}
+#endif
+}
+
 #if 0 /******* GC553 *******/
 
 void avm_ap_version_read(unsigned char* pdata,unsigned short size)	//K18.8.A
diff --git a/project/libavt/avm_spi_flash.h b/project/libavt/avm_spi_flash.h
index 36f98e5..348bef0 100644
--- a/project/libavt/avm_spi_flash.h
+++ b/project/libavt/avm_spi_flash.h
@@ -157,15 +157,18 @@ typedef struct _AVM_FLASH_DEVINFO_OBJ
 
 typedef struct _AVM_CUSTOMER_USAGE_BLOCK
 {
-	unsigned char sn[EXT_VERSION_SN_LEN];
-	unsigned char reserved;
-	unsigned char unused[SPI_FLASH_BLOCK_SZ - EXT_VERSION_SN_LEN - 1];
+	unsigned char sn[EXT_VERSION_SN_LEN];	/* byte 0..12: serial number
+											*/
+	unsigned char configs[8];	/* byte 13/bit 0: HDCP handshake. 0: disable, 1: enable. The rest of the bits are not used.
+								*/
+	unsigned char unused[SPI_FLASH_BLOCK_SZ - EXT_VERSION_SN_LEN - 8];
 } __attribute__((packed)) AVM_CUSTOMER_USAGE_BLOCK, *AVM_CUSTOMER_USAGE_BLOCK_HANDLE;
 
 void avm_gpio_init(void);
 void avm_spi_init(void);
 void avm_usb_sn_get(unsigned char* pdata,unsigned short size);
 void avm_usb_sn_set(unsigned char* pdata,unsigned short size);
+void avm_customer_usage_block_set_byte(unsigned char *pdata, unsigned offset, unsigned size);
 void avm_spi_read_write(unsigned char* buffer,unsigned int isRead);
 void avm_spi_erase(unsigned char cmd, unsigned int addr);
 void avm_ap_version_write(unsigned char* pdata,unsigned short size);
diff --git a/project/libavt/avm_uvc_req.c b/project/libavt/avm_uvc_req.c
index 6e8856b..c998f20 100644
--- a/project/libavt/avm_uvc_req.c
+++ b/project/libavt/avm_uvc_req.c
@@ -7,6 +7,7 @@
 #include "iTE6805_DRV.h"
 #include "gpio.h"
 #include "avt_gpio.h"
+#include "avm_config.h"
 
 #define AVM_UX_HDMI_PLUG_5V 0
 #define AVM_UX_HDMI_READY 1
@@ -66,7 +67,7 @@ void avm_ext_info_recv(unsigned char* pdata)
 		//avm_68051_rdwr(recv_info.factory_init,recv_info.rec_behavior[1],recv_info.rec_behavior[0]);
 		//addr = (unsigned short)(recv_info.rec_behavior[1]<<8)+recv_info.rec_behavior[0];
 //		avm_nuc_hdcp_write(recv_info.hdcp);		//K12.6.A
-		//CyU3PDebugPrint(4,"\n write hdcp?(%d)\r\n",recv_info.hdcp);
+		CyU3PDebugPrint(4,"write hdcp:%d\r\n",recv_info.hdcp);
 		
 #if 0 /* set HDCP block in ITE 68051 to unreachable address 0x76 on DDC bus */
 		unsigned char regval = hdmirxrd(0xCB);
@@ -81,15 +82,35 @@ void avm_ext_info_recv(unsigned char* pdata)
 		}
 #else
 		unsigned char regval = hdmirxrd(0x23);
+		CyU3PDebugPrint(4,"read hdcp:%02x\r\n", regval);
 		unsigned char is_hdcp_in_reset = (regval & 0x2) >> 1;
-		if (recv_info.hdcp) /* enable; out of reset */
+
+		if (recv_info.hdcp) /* enable HDCP handshake; out of reset */
 		{
 			if (is_hdcp_in_reset) hdmirxwr(0x23, regval & 0xFD);
+
+#if 0 /* write to flash */
+			if (!g_avm_config.is_hdcp_handshake)
+			{
+				g_avm_config.is_hdcp_handshake = 1;
+				avm_customer_usage_block_set_byte(&(g_avm_config.is_hdcp_handshake), 13, 1);
+			}
+#endif
 		}
-		else /* disable; put to reset */
+		else /* disable HDCP handshake; put to reset */
 		{
-			if (!is_hdcp_in_reset) hdmirxwr(0x23, regval | 0x2);
-		}
+			if (!is_hdcp_in_reset) hdmirxwr(0x23, regval | 0x2);		
+			
+#if 0 /* write to flash */
+			if (g_avm_config.is_hdcp_handshake)
+			{
+				g_avm_config.is_hdcp_handshake = 0;
+				avm_customer_usage_block_set_byte(&(g_avm_config.is_hdcp_handshake), 13, 1);
+			}
+#endif
+		}		
+		
+		//CyU3PDebugPrint(4,"g_avm_config.is_hdcp_handshake:%d\n", g_avm_config.is_hdcp_handshake);
 #endif
 	}
 	else if (trigger & (1<< UVC_EXT_INFO_FACTROY))	//set factory init
@@ -256,11 +277,11 @@ void avm_ext_info_send(unsigned char* pdata)
 	if (is_addr_76) ext->send_info.hdcp = 0;
 	else ext->send_info.hdcp = 1;
 #else
-	unsigned char regval = hdmirxrd(0x23); /* 1: HDCP logic in reset; 0 otherwise */
+	unsigned char regval = hdmirxrd(0x23); /* [bit 1] 1: HDCP logic in reset; 0 otherwise */
+	CyU3PDebugPrint(4,"read hdcp:%02x\r\n", regval);
 	if (regval & 0x2) ext->send_info.hdcp = 0;
 	else ext->send_info.hdcp = 1;
 #endif
-	//CyU3PDebugPrint(4,"\n read hdcp?(%d)\r\n",ext->send_info.hdcp);
 
 	memcpy(pdata,&ext->send_info,sizeof(AVM_UVC_EXT_INFO_OBJ));
 }
diff --git a/project/libavt/avm_version.c b/project/libavt/avm_version.c
index 672a6f6..d25cc91 100644
--- a/project/libavt/avm_version.c
+++ b/project/libavt/avm_version.c
@@ -1,4 +1,5 @@
 #include "version.h"
+#include "avm_config.h"
 
 const unsigned char g_package_version[]=
 {
@@ -16,3 +17,5 @@ const unsigned char *g_main_version[]=
 	BUILD_DATE,
 	BUILD_HOUR
 };
+
+avm_config_t g_avm_config;
 

 
 
---------------------------------------------------------------------

## 2021/01/08 (FI)



_fusb300_framework_clear_feature
fusb300_set_cxstall

[2021-01-07 18:11:43.994] fusb300_ep0
[2021-01-07 18:11:44.009]   clear_feature
[2021-01-07 18:11:44.009]   Cx request error!! 
[2021-01-07 18:11:44.009] [avm_setup_is_done] val=1

detach

uvc.c Qoo
_fusb300_set_vbus();

GC553: Cypress FX3 Camera Kit header file (uvc.h)

uvc_timer_to_pts
	us = timer / 150;
	pts = us * 100000;
	
	
---------------------------------------------------------------------
## 2021/01/07 (TH)

uvc_main_video_hdmi > fusb300_enable_ep_fifo_int
uvc_main_audio_hdmi_in > fusb300_enable_ep_fifo_int

3.1.1	Internal Direct Memory Access (IDMA) Controller
used to perform fast-block transfers between any two memories local

3.1.2	Enhanced Direct Memory Access (EDMA3) Controller
the device/system DMA controller. Its primary purpose is to service user programmed data transfers between internal (DSP L1/L2, Shared RAM) and external (SDRAM, DDR2/mDDR, or flash memory) or memory-mapped peripherals (like serial ports, MMC/SD etc).


[2021-01-06 20:03:57.369] --------------------------------------
[2021-01-06 20:03:57.369] USB Info
[2021-01-06 20:03:57.369] Format index = 1, Frame index = 1, Width = 1920, Height = 1080
[2021-01-06 20:03:57.369] FrameInterval = 0x00030D40, Frame Rate = 50
[2021-01-06 20:03:57.369] --------------------------------------

--- fusb300_framework_ep0out / (setcur_VideoStreamInterface_commit == 1) ---
[2021-01-06 20:03:57.369] disable EP3 INT
[2021-01-06 20:03:57.369] Video State : -> Prepare MSG
[2021-01-06 20:03:57.369] ------------------------------------------------------
[2021-01-06 20:03:57.369] loadMSG : (BLACK_SCREEN)
[2021-01-06 20:03:57.418] Warning MSG Mem = 0x03400000
[2021-01-06 20:03:57.557] Load Warning MSG done

--- fusb300_enable_ep_fifo_int() ---
[2021-01-06 20:03:57.557] enable EP3 INT

[2021-01-06 20:03:57.557] Video State : Prepare MSG->Check HDMI
[2021-01-06 20:03:57.557] fusb300_ep0
[2021-01-06 20:03:57.557]   clear_feature
[2021-01-06 20:03:57.557] Clear Feature : U2_ENABLE
[2021-01-06 20:03:57.557] fusb300_ep0
[2021-01-06 20:03:57.557]   set_interface

--- _fusb300_framework_set_interface() ---
[2021-01-06 20:03:57.557] Audio HDMI State : ->Prepare Start

--- fusb300_enable_ep_fifo_int() ---
[2021-01-06 20:03:57.557] enable EP1 INT

--- uvc_main_audio_hdmi_in() ---
[2021-01-06 20:03:57.557] uvc_main_audio_hdmi_in uvc_iso_in_HDMI_Status=1,uvc_iso_out_DAC_Status=0
[2021-01-06 20:03:57.557] Audio HDMI State : Prepare->Sync

S/N: 1 35 31 30 30 33 33 33 36 30 30 30 30 38
S/N: 1 35 31 30 30 33 33 33 36 30 30 30 33 33
S/N: 1 35 31 30 30 33 33 33 36 30 30 30 33 36
S/N: 1 35 31 30 30 33 33 33 36 30 30 30 30 31
S/N: 1 35 31 30 30 33 33 33 36 30 30 30 31 36
S/N: 1 35 31 30 30 33 33 33 36 30 30 30 30 35
S/N: 1 35 31 30 30 33 33 33 36 30 30 30 30 37
S/N: 1 35 31 30 30 33 33 33 36 30 30 30 30 36
S/N: 1 35 31 30 30 33 33 33 36 30 30 30 31 34

[2021-01-06 20:04:04.411] USB :	width = 1920, height = 1080
[2021-01-06 20:04:04.411] Capture Input : YUV444DP
[2021-01-06 20:04:04.411] Capture0->DDR->USB
[2021-01-06 20:04:04.411] Output format : NV12
[2021-01-06 20:04:04.411] frcMode CAPTURE_FRC_MODE_1
[2021-01-06 20:04:04.411] Capture 0 Flow Control Enable
[2021-01-06 20:04:04.411] ------------------------------------------------------
[2021-01-06 20:04:04.411] Video State : Check HDMI->Update Video
[2021-01-06 20:04:04.411] Video State : Update Video->Stable

uvc_main_audio_hdmi_in > Clear_HDMI_RingBuffer
[2021-01-06 20:04:04.411] Clear_HDMI_RingBuffer
[2021-01-06 20:04:04.411] IT68051 SampleRate = 3
[2021-01-06 20:04:04.411] Audio HDMI State : Sync->Stable


typedef enum
{
	UVC_VIDEO_STATE_STANDBY,
	UVC_VIDEO_STATE_PREPARE_MSG,		
	UVC_VIDEO_STATE_CHECK_HDMI,		
	UVC_VIDEO_STATE_UPDATE_VIDEO,			/* 3 */
	UVC_VIDEO_STATE_STABLE
} UVC_VIDEO_STATE;

typedef enum
{
	UVC_AUDIO_STATE_STANDBY,
	UVC_AUDIO_STATE_PREPARE_START,
	UVC_AUDIO_STATE_PREPARE_STOP,
	UVC_AUDIO_STATE_SYNC,			//HDMI Video + Audio, or ADC Audio /* 3 */
	UVC_AUDIO_STATE_CHECK_HDMI,		//HDMI Audio
	UVC_AUDIO_STATE_STABLE
} UVC_AUDIO_STATE;

portableapps: HDHacker, MBR and boot sector manager

---------------------------------------------------------------------

## 2021/01/06 (WE)

1/002-程式規劃、撰寫、測試/板端廠測程式/BU113/-/4/裝置被占用
1/002-程式規劃、撰寫、測試/板端廠測程式/BU113/-/2/ER330 add copy log, release document
0/開會/1/部門會議
0/開會/1/BU113 bug review

syslogd -l 8 -D -s 2048 -b 3 -O /var/log/messages
klogd -c 8

入測試失敗原因的代碼、失敗備份LOG、加入失敗重測：錄影開始、讀取設定RTC、讀取MCU版本




UVC_VIDEO_STATE g_uvc_video_state
UVC_AUDIO_STATE g_uvc_audio_HDMI_state


uvc_dynamic_chg_hdcp(uint8_t on)


Clear AllEndPoint


---------------------------------------------------------------------

## 2021/01/05 (TU)

1/002-程式規劃、撰寫、測試/板端廠測程式/BU113/-/8/HDCP handshake設定要寫入FLASH，初始化時要讀出(未完)





## 2021/01/04 (MO)


工作週誌資料維護
人員 A003257 丁家駿
部門 TWA00335 研發九部
項次/工作項目/工作內容/產品/客戶/作業時數/備註

1/002-程式規劃、撰寫、測試/板端廠測程式/ER330/-/8/加入測試失敗原因的代碼、加入失敗重測：錄影開始、讀取設定RTC、讀取MCU版本









## 2020/12/31 (TH)




大前研一「從0到1」的發想術：商業突破大學最精華的一堂課，突破界限從無到有的大前流思考法










## 2020/12/30 (WE)





重要提醒
你不需要很厲害才能開始，但你需要開始才會很厲害
我做我知道可以做的，上帝就會做我不知道、不能做的
大量閱讀、時常寫作、隨手整理
定時反省檢討
---------------
2021 Q1 

Objective: USB/UVC/UAC
Key Results:



Objective: 讀資料結構FUNDAMENTALS OF DATA STRUCTURES IN C++第一章到第五章
Key Results:
整理筆記
課本習題親手做一遍


暖心書單/計畫細節
Clear, Atomic Habits: An Easy & Proven Way to Build Good Habits & Break Bad Ones 克利爾 原子習慣：細微改變帶來巨大成就的實證法則


---------------

## 2020/12/30 (WE)


commit bb4c1bc8d6cad47d0182392e58b83d51df0ec756 (HEAD -> er330_beta)
Author: Joel Ding <joel.ding@avermedia.com>
Date:   Wed Dec 30 16:21:37 2020 +0800

    add autotest record.
            new file:   mainrec.c

    Change-Id: Ic4d0aea4ba4a6e6ed9606887a15c293fff7423c0



## 2020/12/28 (MO)


GraphStudioNext


HDMIRX_AUDIO_STATE UVC_HDMI_ASTATE_ON


## 2020/12/26 (SA)


http://ocw.nthu.edu.tw/videosite/index.php?op=watch&id=8244&filename=854_480_768.MP4&type=download&cid=252&chid=2772

GA: Google Anaysltic

* Notepad++ remove [Unwanted syntax Highlighting for Markdown](https://stackoverflow.com/questions/56722670/notepad-unwanted-syntax-highlighting-for-markdown): Remove Notepad++\userDefineLangs\
* add wysiwyg [在Notepad++中使用Markdown](https://www.itread01.com/content/1543489339.html) [MarkdownViewerPlusPlus-0.8.2-x86.zip
](https://github.com/nea/MarkdownViewerPlusPlus/releases/download/0.8.2/MarkdownViewerPlusPlus-0.8.2-x86.zip)

1.http://www.lintcode.com/zh-cn/problem/

有面試真題，階梯訓練，比賽等模組

2.https://leetcode.com/

很火的演算法題庫，線上答題，討論

知乎搜尋演算法訓練網站，提供了很多網址，但是這兩個網站的演算法題用來入門比較好。共勉！

高點、大碩

## 2020/12/25 (FR)


1. resolution
2. frame rate
3. digital representation
4. system colorimetry

- [BT.601](https://en.wikipedia.org/wiki/Rec._601)
  - target at SDTV
- [BT.709](https://en.wikipedia.org/wiki/Rec._709)
  - target at HDTV
- [BT.2020](https://en.wikipedia.org/wiki/Rec._2020)
  - target at UHDTV with SDR
  - a bit depth of either 10 bits per sample or 12 bits per sample
- [BT.2100](https://en.wikipedia.org/wiki/Rec._2100)
  - target at HDTV and UHDTV with HDR

- BT.656: ITU-R Recommendation for parallel and serial transmission formats for BT.601 video

- chromaticities: 
  - color characteristics
 
http://opensource.rock-chips.com/wiki_Main_Page
 
https://docs.microsoft.com/en-us/windows/win32/audio-and-video


git clone "ssh://a003257@CodeReview-New.avermedia.com:29418/Embedded_FW/IT9325/BU113" && scp -p -P 29418 a003257@CodeReview-New.avermedia.com:hooks/commit-msg "BU113/.git/hooks/"

Computer Display Monitor Timing (DMT)
VESA Coordinated Video Timings (CVT) https://glenwing.github.io/docs/VESA-CVT-1.2.pdf
CVR is short for CVT-R which is the Coordinated Video Timings. Yes, used to reduce blanking


---------------------------------------------------------------------




`````````````````````````````````````````````````````````````````````

2020/12/24 (TH)

Video Format 影像格式 NV12

https://github.com/avt-a003257/avt-a003257.github.io.git

gem 'github-pages', '~> 209'
gem install github-pages

https://github.com/avt-a003257/a003257.github.io.git

////////////////////////////////////////////////////////////////////////////

2020/12/23 (WE)

------------------------
loadMSG : Not Support
......
Load Marning MSG done
------------------------

_uvc_prepareMSG
if (g_uvc_usb_info.width == 1920 && g_uvc_usb_info.height == 1080)	
_uvc_loadMSG_NV12
_uvc_loadMSG_YUY2
_uvc_loadMSG_P010

_uvc_updateVideoStream

g_uvc_video_mode == UVC_VIDEO_MODE_NOT_SUPPORT
g_uvc_usb_info.frameRate
g_res_hdmi[]


g_fusb300_dev_mode
FUSB300_DEVICE_MODE_SS_MODE
////////////////////////////////////////////////////////////////////////////

2020/12/22 (TU)



蔡仁松教授資料結構
http://ocw.nthu.edu.tw/ocw/index.php?page=chapter&cid=252&chid=2772

韌體 0.0.0.4 (不含)以上修正

USB 裝置晶片型號查詢工具 https://zhtwnet.com/chipgenius/


////////////////////////////////////////////////////////////////////////////

2020/12/21 (MO)


NTFS-3G https://en.wikipedia.org/wiki/Ntfsprogs
ntfsfix
https://www.tuxera.com/company/open-source/




Silberschatz, Abraham; Galvin, Peter Baer; Gagne, Greg (2002). Operating System Concepts


VOLUME_IS_DIRTY
vol->flags
ntfsprogs/utils.c

vol = ntfs_device_mount(dev, NTFS_MNT_RDONLY);
if (!vol)

replay_log(vol);

if (vol->flags & VOLUME_IS_DIRTY)




請問：

測試使用的存儲裝置，是128GB的U盤嗎？是否可以列出型號？
測試過程是否
這支U盤看起來是exFAT的格式，可是掛載時卻用NTFS的參數。請問裝置本身功能是正常的嗎？

以Windows 10/OBS 26.0.2測試3840x2160@30
來源：CHROMA 2238
韌體 0.0.0.3 (含)以上支援

////////////////////////////////////////////////////////////////////////////

2020/12/19 (SA)

ufsd_is_dirty()




////////////////////////////////////////////////////////////////////////////

2020/12/18 (FR)

IT932x_RomEditor.exe 71c5c02d881f7d6c2de2028c25abf9f9 >> SAME







進修書單

工作書單



QHD (Quad HD), WQHD (Wide Quad HD), or 1440p, is a display resolution of 2560 × 1440 pixels in a 16:9 aspect ratio. 

https://music.stackexchange.com/questions/3711/is-there-any-midi-software-that-can-display-in-real-time-the-notes-i-play-next-t

Video Timings Calculator Aug 3, 2019 https://tomverbeure.github.io/video_timings_calculator
Pixel Clock Calculator https://www.monitortests.com/pixelclock.php



Where in EDID is about HDR?


Video Demystified: A Handbook for the Digital Engineer, 5th Edition (May 14, 2007) by Keith Jack

////////////////////////////////////////////////////////////////////////////

2020/12/17 (TH)



3840x2160P60 HDR	TIMING:721;PATTERN:1020 [o]
3840x2160P59.94 HDR	
3840x2160P60	TIMING:721;PATTERN:201 [with QD908v2]
3840x2160P59.94	TIMING:721 [o]
3840x2160P30	TIMING:687 [o]
3840x2160P29.97	TIMING:686 [o]

2560x1440P60 HDR		[temp no test on this]
2560x1440P59.94 HDR	
2560x1440P144	[o]
2560x1440P60	[temp no test on this]
2560x1440P59.94	

1920x1080P240	[o]
1920x1080P60 HDR		TIMING:632;PATTERN:1020 [o]
1920x1080P59.94 HDR		TIMING:631;PATTERN:1020 [o]
1920x1080P120	TIMING:702 [o]
1920x1080P60	TIMING:632 [o]
1920x1080P59.94	TIMING:631;PATTERN:201 [o]
1920x1080P50

1280x720P60		TIMING:608;PATTERN:201 [o]
1280x720P59.94	TIMING:607;PATTERN:201 [o]
1280x720P50

720x576P50		TIMING:633 [o]

720x480P60		TIMING:604 [o]
720x480P59.94	TIMING:603 [o]

640x480P60	TIMING:602 [o] QD881:DMT0660 [v]
640x480P59.94 TIMING:601 [o] QD881:DMT0659 [v]

1920x1080i60	TIMING:610;PATTERN:201 [o]
1920x1080i59.94		TIMING:609;PATTERN:201 [o]

720x576i		TIMING:637/638;PATTERN:201 [o]

720x480i60	TIMING:612/614;PATTERN:201 [o]
720x480i59.94	TIMING:611/613;PATTERN:201 [o]


g_uvc_video_mode == UVC_VIDEO_MODE_NOT_SUPPORT









https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/fsutil-dirty
Queries or sets a volume's dirty bit.




////////////////////////////////////////////////////////////////////////////

2020/12/16 (WE)


https://openhome.cc/Gossip/CppGossip/Constructor.html
in-class initializer
default: 提供無參建構式，其行為與預設建構式相同
constructor initializer list
初始式清單的順序並不代表值域初始化的順序，值域初始化的順序是依類別中值域定義的順序而定。
	AVM_LED_OFF, AVM_LED_ON, AVM_LED_NORMAL, AVM_LED_BOOTING, AVM_LED_LOST_SIGNAL, AVM_LED_IS_HDCP, AVM_LED_UPGRADING, AVM_LED_UPGRADE_SUCCESS, 	AVM_LED_UPGRADE_FAILURE




世界記憶力冠軍的高效記憶筆記 Gunther Karsten
圖解合成器入門

Illustrated C# 7: The C# Language Presented Clearly, Concisely, and Visually Daniel Solis
Building Evolutionary Architectures: Support Constant Change Neal Ford, Rebecca Parsons, Patrick Kua


Linux for Developers: Jumpstart Your Linux Programming Skills William Rothwell



////////////////////////////////////////////////////////////////////////////

2020/12/15 (TU)

:: 類別範圍解析（class scope resolution）運算子
this 指標


1080P60, 4KP30


////////////////////////////////////////////////////////////////////////////

2020/12/14 (MO)

ithTimerGetCounter()
韌體版本0.0.0.2(不含)以上修正
	BU113 LED Definition	
idx	Item	Power 燈號
0	AVM_LED_OFF	藍燈紅燈均暗
1	AVM_LED_ON	N/A
2	AVM_LED_NORMAL	藍燈恆亮
3	AVM_LED_BOOTING	藍燈閃爍
4	AVM_LED_LOST_SIGNAL	紅燈恆亮
5	AVM_LED_IS_HDCP	紅燈恆亮
6	AVM_LED_UPGRADING	藍燈閃爍
7	AVM_LED_UPGRADE_SUCCESS	恆亮 (藍燈或紅燈)
8	AVM_LED_UPGRADE_FAILURE	藍燈紅燈交替閃爍

////////////////////////////////////////////////////////////////////////////

2020/12/11 (FR)

hdcp_ver

編曲

D:\avt\BU113\src\build\openrtos\HDMI_Bridge\lib\fa626

////////////////////////////////////////////////////////////////////////////

2020/12/09 (WE)



fusb300_framework_ep0out len:34
00 00 01 03 0a 8b 02 00 00 00 00 00 00 00 00 00 00 00 00 d8 bd 00 00 40 00 00 00 00 00 00 00 00 00 00

00 00 01 03 0a 8b 02 00 00 00 00 00 00 00 00 00 00 00 00 d8 bd 00 00 40 00 00 00 00 00 00 00 00 00 00

////////////////////////////////////////////////////////////////////////////

2020/12/09 (WE)

* 932x datasheet



00 00 04 01 40 0d 03 00
00 00 00 00 00 00 00 00
00 00 00 d8 bd 00 00 40
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00

00 00 04 01 40 0d 03 00
00 00 00 00 00 00 00 00
00 00 00 d8 bd 00 00 40
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00

Table 4-75 Video Probe and Commit Controls 


ITE932x supports NV12, YUY2, RGB32, P010 output formats 
在DirectShow中，常见的RGB格式有RGB1、RGB4、RGB8、RGB565、RGB555、RGB24、RGB32、ARGB32等；常见的YUV格式有YUY2、YUYV、YVYU、UYVY、AYUV、Y41P、Y411、Y211、IF09、IYUV、YV12、YVU9、YUV411、YUV420等。作为视频媒体类型的辅助说明类型（Subtype），它们对应的GUID见表2.3。 https://blog.csdn.net/zoutian007/article/details/7585511

色彩採樣 (Chroma subsampling) https://zh.wikipedia.org/wiki/%E8%89%B2%E5%BA%A6%E6%8A%BD%E6%A0%B7

Getting the correct RGB color range out of your Elgato capture card in OBS Studio http://ltroyalshrimp.com/getting-the-correct-rgb-color-range-out-of-your-elgato-capture-card-in-obs-studio/

Partial/limited RGB: the 16-235 color range in TV broadcast signals
Full RGB: 0-255 signals in modern day TVs and PC monitors 


YUV video is simply always limited range (16 black point, 235 white point)


韌體版本0.0.0.2(不含)以上修正
因為PNPID相同，Windows需手動移除驅動、重開機以後再測試，避免系統記得上一次的裝置敘述。


In: RGB 4:4:4 Full; out: OBS set as partial >> 0:255
00 00 01 03 0a 8b 02 00
00 00 00 00 00 00 00 00
00 00 00 d8 bd 00 00 40
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00

In: RGB 4:4:4 Full; out: OBS set as full >> 16:235
00 00 01 03 0a 8b 02 00
00 00 00 00 00 00 00 00
00 00 00 d8 bd 00 00 40
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00

In: RGB 4:4:4 Limited; out: OBS set as partial >> 0:255
00 00 01 03 0a 8b 02 00
00 00 00 00 00 00 00 00
00 00 00 d8 bd 00 00 40
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00

In: RGB 4:4:4 Limited; out: OBS set as full >> 16:235
00 00 01 03 0a 8b 02 00
00 00 00 00 00 00 00 00
00 00 00 d8 bd 00 00 40
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00

HDMIRX_HDCP_STATE
iTE6805_HDCP_Detect();
HDCP_ENABLE
HDCP_DISABLE

HDMIRXSetProperty()
////////////////////////////////////////////////////////////////////////////

2020/12/08 (TU)


ITE HDMI 4K+ Bridge
49 54 45 20 48 44 4d 49 20 34 4b 2b 20 42 72 69 64 67 65

ExtremeCap 4K
45 78 74 72 65 6d 65 43 61 70 20 34 4b

 High Dynamic Range (HDR) to 
 
 Standard Dynamic Range (SDR) 
using a conventional gamma curve

iTE6805_Enable_Video_Output()



avm_hdmirx_color_range_get
avm_fpga_csc

5.3.94   HDR2SDR (+0x17C) 
Default Value: 0x0D490000 
Field  Bits  Type  Description 
YUV2RGB_33  12:0  RW  Fixed-point representation of CI 33  of YUV2RGB Equation. 
2020TO709_11  28:16  RW  Color gamut mapping parameter. 
 
5.3.95   HDR2SDR (+0x180) 
Default Value: 0x1F6B1B4D 
Field  Bits  Type  Description 
2020TO709_12  12:0  RW  Color gamut mapping parameter. 
2020TO709_13  28:16  RW  Color gamut mapping parameter. 

////////////////////////////////////////////////////////////////////////////

2020/12/07 (MO)


USB 3.0相容性測試

分為兩個類別，裝置端（device）與主機端（host）。

在裝置端的部分，必須通過「互通性測試」（xHCI Interoperability test）的檢驗，其主要是針對所有USB 3.0的產品架構所作的裝置互通性測試，讓各種USB 3.0產品能與其他裝置有效地互通並協同運作，不會因為軟、硬體版本的不同而失效。

在主機端部分，除了作互通性測試外，還得進行另一項名為「向後兼容測試」（xHCI Backwards compatibility test）的驗證，其測試標的除了整個USB產品架構外，xHCI controller還必須與現不同的USB產品（known good device）作測試，以確保不同的USB產品在這個主機端上能夠正常的運作。

我們可以發現，USB 3.0的推出除了代表速度與效能的技術提升外，為了確保與前代技術與裝置的相容性，類似的互通性與向後兼容測試勢必非常重要，才能讓原本的USB技術維持零落差的技術條件與使用情境。與USB 2.0測試不同的是，某些測試上的問題肇因是單單發生在USB 3.0測試當中，這也意味著即使USB 2.0已高普及化，但在實際驗證USB 3.0時還是會遇到許多新的難題，值得廠商與我們去一一克服和疑難排解。

https://www.allion.com.tw/usb-3-0%E5%AF%A6%E6%B8%AC%E8%A9%95%E9%91%91%E8%88%87%E5%A0%B1%E5%91%8A%EF%BC%9A%E5%BF%AB%E9%80%9F%E9%A0%98%E7%95%A5%E5%95%8F%E9%A1%8C%E7%99%A5%E7%B5%90%E8%88%87%E8%A7%A3%E6%B1%BA%E6%96%B9%E6%A1%88/

5.3.43 (+0x0A8)
WrDir 17:16 1: mirror mode; 2: flip mode
IOWrRotDir 12:10 100: mirror; 101: flip
CAP_REG_GSR8_BIT_WR_DIR
ithWriteRegA(CAP0_BASE + CAP_REG_GSR8, );

1. 願神醫治與救恩臨到加護病房中重病的姑媽(曾憲芳,曾經受洗後來拜偶像)以及卵巢惡瘤後天開刀的同學(郭育孜,參加過2次福音活動)
2. 左手關節鈣化 發炎 退化 求神憐憫醫治
3.胚胎/染色體/基因健康並著床順利，求神賞賜我神給莎拉的恩典與信心。

NUC_AP_REG_HDCP_VER 0x21, bit 3
SetHDCPLevel

capture0_init

	g_uvc_video_state = UVC_VIDEO_STATE_PREPARE_MSG;


1.求主能保守承恩各器官穩定發展跟足月寶寶一樣。開始復健時能有明顯的果效承恩也不會排斥跟不舒服，保留體力來成長跟復健，每天能睡的香甜。
2.冠弘和雅藍穩定靈修
3.2020年業績達標。
4.小組與家人能夠身體健康，心中平安。
5.求主供應家中經濟一切的需要，保守冠弘有足夠的體力與精神使他能夠面對工作與照顧妻小.
6.雅藍的身體可以恢復穩定運動，也為我的財務與工作是否復職禱告，求神帶領。
7.冠弘轉換新單位可以得心應手，學習新的資訊可以有效吸收。
8.皮膚跟免疫系統可以越來越好，皮膚不再受傷。
9.左手手腕發炎求主使我的手能遇到對的醫生來恢復。


想參加減肥名醫劉才睿的講座，再跟我說哦
活動由教會小組舉辦，無須加入教會就可參加。因場地限制，出席活動需報名


 extern unsigned char g_avm_uvc_is_commit;




HDMI支援非壓縮的8聲道數位音頻傳送(取樣率192kHz，資料長度24bits/sample)，以及任何壓縮音頻串流如Dolby Digital或DTS，亦支援SACD所使用的8聲道的1bit DSD信號。在HDMI 1.3規格中，又追加了超高資料量的非壓縮音頻串流如Dolby TrueHD與DTS-HD的支援。



////////////////////////////////////////////////////////////////////////////

2020/12/03 (TH)

AVM_EXTENSION_ID_INFO



P0_HDCPDDCIDLE reg 15:7


P0_EnHDCPRst 23:6 


D6:6
Deinterlacing
https://www.intel.com/content/dam/www/programmable/us/en/pdfs/literature/wp/wp-01117-hd-video-deinterlacing.pdf

An interlaced video is a succession of 50/60 fields per second, where each field carries only half of the rows that are displayed in each frame of video.
one frame of video is broken into two fields, one of which contains the even lines and the other the odd lines

two basic deinterlacing methods are commonly referred to as “bob” and “weave.”
 spatial line doubling
 
 
Motion adaptive

////////////////////////////////////////////////////////////////////////////

2020/12/02 (WE)

  0  1  2  3  4  5  6  7
 01 01 02 D0 05 00 0C 3C 
 00 00 00 02 02 04 00 00 
 00 00 00 00 00 00 00 00 
 00 00 00 00 00 00 00 00

////////////////////////////////////////////////////////////////////////////

2020/12/02 (WE)


AUDIO_IS_NOT_ON
AUDIO_FORMAT_HBR
AUDIO_FORMAT_DSD
AUDIO_FORMAT_NLPCM
AUDIO_FORMAT_LPCM

else if (setcur_VideoStreamInterface_commit == 1)

fusb300_framework.c@2157
		g_uvc_video_state = UVC_VIDEO_STATE_PREPARE_MSG;
		g_uvc_usb_info.ap_off_count = 0;
		printf("Video State : -> Prepare MSG\n");
		fusb300_set_cxdone();



////////////////////////////////////////////////////////////////////////////

2020/12/01 (TU)

iTE6805_DATA.DRM_DB[0]

avm_ext_hdr_data_set(hdr);
//avm_ext_hdr_meta_set(hdr, &iTE6805_DATA.DRM_HB[0], &iTE6805_DATA.DRM_DB[0]); 

memcpy(, ext->hdr_meta, sizeof(ext->hdr_meta));

////////////////////////////////////////////////////////////////////////////

iTE6805_DATA.Force_Sampling_Frequency

HDR Enable: It specifies if executing the HDR function. 
HDR EOTF: It specifies the HDR format for execution. 

High Dynamic Range Imaging
HDR10: HDR格式最基本以及最普及的

EOTF (Electro-Optical Transfer Function)：SMPTE ST 2084
Color Sub-sampling：4:2:0（壓縮影片）
Bit Depth：10 bit
色域：ITU-R BT.2020
Metadata（元數據）：SMPTE ST 2086、MaxFALL、MaxCLL

AVM_RES_HDMI_IDX


				HDMIRX_DEBUG_PRINT(("Flag_VidStable_Done!=TRUE, Save AVI Infoframe to variable. \n" ));
				HDMIRX_DEBUG_PRINT(("AVIDB1 = %x \n", AVIDB ));
				HDMIRX_DEBUG_PRINT(("prevAVIDB1 = %x \n", prevAVIDB ));
				prevAVIDB = AVIDB ;

uvc.c@3390
struct UVC_HDMI_Info g_uvc_hdmi_info[2];
uvc_getHDMIinfo()


CyU3PDebugPrint(0, "\r\n", ...);
CyU3PDebugPrint(priority, fmt, args...) printf("%s@%d " fmt, __func__, __LINE__, ##args)

fusb300_framework.c@1729 
fusb300_framework.c@2162


set_ApRegWrite

			setreport = 1; //Wait CXout for data stage
			setreport_len = setup_pkt.wLength;


1  5  1  0  0 3   3  3  6  0  0  0  2  1 14 b 1b 15 0 0 0 0 0 0 0 1 0 0
0 FF FF FF FF FF FF FF FF FF FF FF FF FF 14 B 1B F 0 0 0 0 0 0 0 1 0 0
0 FF FF FF FF FF FF FF FF FF FF FF FF FF 14 B 1B 10 0 0 0 0 1 0 0 1 0 0

avm_g_enableWriteSerialNum

	mmpIicReceiveData(IIC_PORT_0, IIC_MASTER_MODE, (g_slave_addr >> 1), wBuf, 1, rBuf, 1);


NV12
YUY2
P010



1.物件導向分析設計基本概念 。
2.類別與物件。
3.建構元與解構元∕資料成員與成員函式∕this指標。
4.Static資料成員∕static成員函式。
5.朋友函數/朋友類別與iterator class。
6.繼承與衍生類別的使用。
7.虛擬函式與多型∕case study。
8.Call by value V.S. call by reference。
9.動態記憶體配置與釋放。
10.Copy constructor與operator assignment。
11.Embedded object。
12.變數型別轉換與conversion constructor。
13.簡介C++/MFC類別庫。
14.Ｃ和C++的互通。
15.多親繼承∕虛擬基礎類別。
16.改變運算子定義。
17.樣版-template與STL樣版類別庫
18.認識TR1 Extension, C++0x, 和C++ 11的新語法

////////////////////////////////////////////////////////////////////////////

2020/11/23 (MO)


build\openrtos\HDMI_Bridge\project\HDMI_Bridge\HDMI_Bridge.bin
build\openrtos\HDMI_Bridge\project\bootloader\bootloader.bin

fusb300_framework.c@1705 extension unit id 0x3, interface id 0x0, wIndex=0x300


Device Descriptor:
bcdUSB:             0x0300
bDeviceClass:         0xEF
bDeviceSubClass:      0x02
bDeviceProtocol:      0x01
bMaxPacketSize0:      0x09 (9)
idVendor:           0x07CA
idProduct:          0x1113
bcdDevice:          0x0100
iManufacturer:        0x01
0x0409: "ITE"
iProduct:             0x02
0x0409: "ITE HDMI 4K+ Bridge"
0x0409: "ITE HDMI 4K+ Bridge"
iSerialNumber:        0x03
0x0409: "00000001"
bNumConfigurations:   0x01

ConnectionStatus: DeviceConnected
Current Config Value: 0x01
Device Bus Speed:     High
Device Address:       0x1B
Open Pipes:              4

Endpoint Descriptor:
bEndpointAddress:     0x82  IN
Transfer Type:   Interrupt
wMaxPacketSize:     0x0040 (64)
bInterval:            0x01

Endpoint Descriptor:
bEndpointAddress:     0x87  IN
Transfer Type:   Interrupt
wMaxPacketSize:     0x0200 (512)
bInterval:            0x0A

Endpoint Descriptor:
bEndpointAddress:     0x81  IN
Transfer Type: Isochronous
wMaxPacketSize:     0x00C0 (192)
bInterval:            0x04

Endpoint Descriptor:
bEndpointAddress:     0x83  IN
Transfer Type:        Bulk
wMaxPacketSize:     0x0400 (1024)
bInterval:            0x00

Configuration Descriptor:
wTotalLength:       0x0352
bNumInterfaces:       0x05
bConfigurationValue:  0x01
iConfiguration:       0x00
bmAttributes:         0x80 (Bus Powered )
MaxPower:             0x32 (100 Ma)

Unknown Descriptor:
bDescriptorType:      0x0B
bLength:              0x08
08 0B 00 02 0E 03 00 02 

Interface Descriptor:
bInterfaceNumber:     0x00
bAlternateSetting:    0x00
bNumEndpoints:        0x01
bInterfaceClass:      0x0E
bInterfaceSubClass:   0x01
bInterfaceProtocol:   0x00
iInterface:           0x02
0x0409: "ITE HDMI 4K+ Bridge"
0x0409: "ITE HDMI 4K+ Bridge"

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x0D
0D 24 01 10 01 51 00 00 E1 F5 05 01 01 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x12
12 24 02 01 01 02 00 00 00 00 00 00 00 00 03 00 
00 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x0D
0D 24 05 02 01 00 00 03 00 00 00 00 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1C
1C 24 06 03 CF 38 A1 7C F2 71 C5 4E 8D 4C F0 87 
74 1C AB AE 18 01 02 03 FF FF FF 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x09
09 24 03 04 01 01 00 03 00 

Endpoint Descriptor:
bEndpointAddress:     0x82  IN
Transfer Type:   Interrupt
wMaxPacketSize:     0x0040 (64)
bInterval:            0x01

Unknown Descriptor:
bDescriptorType:      0x30
bLength:              0x06
06 30 00 00 40 00 

Unknown Descriptor:
bDescriptorType:      0x25
bLength:              0x05
05 25 03 40 00 

Interface Descriptor:
bInterfaceNumber:     0x01
bAlternateSetting:    0x00
bNumEndpoints:        0x01
bInterfaceClass:      0x0E
bInterfaceSubClass:   0x02
bInterfaceProtocol:   0x00
iInterface:           0x00

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x11
11 24 01 04 39 02 83 00 04 00 00 00 01 00 00 00 
00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1B
1B 24 04 01 05 4E 56 31 32 00 00 10 00 80 00 00 
AA 00 38 9B 71 0C 01 10 09 00 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 01 02 00 0F 70 08 00 C0 50 94 00 80 FA 
B1 00 D8 BD 00 15 16 05 00 01 15 16 05 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 02 02 00 0A A0 05 00 00 EB 41 00 00 34 
9E 00 60 54 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 03 02 80 07 38 04 00 30 14 25 00 40 FD 
58 00 76 2F 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 04 02 00 05 D0 02 00 C0 7A 10 00 00 8D 
27 00 18 15 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 05 02 80 02 E0 01 00 40 7E 05 00 00 2F 
0D 00 08 07 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x06
06 24 0D 01 01 01 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1B
1B 24 04 02 04 59 55 59 32 00 00 10 00 80 00 00 
AA 00 38 9B 71 10 01 10 09 00 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 01 03 00 0A A0 05 00 00 E4 57 00 00 F0 
D2 00 80 70 00 40 0D 03 00 01 40 0D 03 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 02 03 80 07 38 04 00 40 70 31 00 00 A7 
76 00 48 3F 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 03 03 00 05 D0 02 00 00 F9 15 00 00 BC 
34 00 20 1C 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 04 03 80 02 E0 01 00 00 53 07 00 00 94 
11 00 60 09 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x06
06 24 0D 01 01 01 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1B
1B 24 04 03 02 50 30 31 30 00 00 10 00 80 00 00 
AA 00 38 9B 71 18 01 10 09 00 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 01 02 80 07 38 04 00 60 28 4A 00 80 FA 
B1 00 EC 5E 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 02 02 00 05 D0 02 00 80 F5 20 00 00 1A 
4F 00 30 2A 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x06
06 24 0D 01 01 01 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1B
1B 24 04 04 03 7E EB 36 E4 4F 52 CE 11 9F 53 00 
20 AF 0B A7 70 20 01 10 09 00 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 01 02 80 07 38 04 00 80 E0 62 00 00 4E 
ED 00 90 7E 00 15 16 05 00 01 15 16 05 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 02 02 00 05 D0 02 00 00 F2 2B 00 00 78 
69 00 40 38 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x1E
1E 24 05 03 02 80 02 E0 01 00 00 A6 0E 00 00 28 
23 00 C0 12 00 0A 8B 02 00 01 0A 8B 02 00 

Unknown Descriptor:
bDescriptorType:      0x24
bLength:              0x06
06 24 0D 01 01 01 

Endpoint Descriptor:
bEndpointAddress:     0x83  IN
Transfer Type:        Bulk
wMaxPacketSize:     0x0400 (1024)
bInterval:            0x00

Unknown Descriptor:
bDescriptorType:      0x30
bLength:              0x06
06 30 0F 00 00 00 

Unknown Descriptor:
bDescriptorType:      0x0B
bLength:              0x08
08 0B 02 02 01 01 00 08 

Interface Descriptor:
bInterfaceNumber:     0x02
bAlternateSetting:    0x00
bNumEndpoints:        0x00
bInterfaceClass:      0x01 (Audio)
bInterfaceSubClass:   0x01 (Audio Control)
bInterfaceProtocol:   0x00
iInterface:           0x08
0x0409: "ITE HDMI 4K+ Bridge"
0x0409: "ITE HDMI 4K+ Bridge"
0x0409: "ITE HDMI 4K+ Bridge"

Audio Control Interface Header Descriptor:
bLength:              0x09
bDescriptorType:      0x24
bDescriptorSubtype:   0x01
bcdADC:             0x0100
wTotalLength:       0x001E
bInCollection:        0x01
baInterfaceNr[1]:     0x03

Audio Control Input Terminal Descriptor:
bLength:              0x0C
bDescriptorType:      0x24
bDescriptorSubtype:   0x02
bTerminalID:          0x01
wTerminalType:      0x0602 (Digital audio interface)
bAssocTerminal:       0x00
bNrChannels:          0x02
wChannelConfig:     0x0003
iChannelNames:        0x00
iTerminal:            0x0A

Audio Control Output Terminal Descriptor:
bLength:              0x09
bDescriptorType:      0x24
bDescriptorSubtype:   0x03
bTerminalID:          0x09
wTerminalType:      0x0101 (USB streaming)
bAssocTerminal:       0x00
bSoruceID:            0x01
iTerminal:            0x00

Interface Descriptor:
bInterfaceNumber:     0x03
bAlternateSetting:    0x00
bNumEndpoints:        0x00
bInterfaceClass:      0x01 (Audio)
bInterfaceSubClass:   0x02 (Audio Streaming)
bInterfaceProtocol:   0x00
iInterface:           0x08
0x0409: "ITE HDMI 4K+ Bridge"
0x0409: "ITE HDMI 4K+ Bridge"
0x0409: "ITE HDMI 4K+ Bridge"

Interface Descriptor:
bInterfaceNumber:     0x03
bAlternateSetting:    0x01
bNumEndpoints:        0x01
bInterfaceClass:      0x01 (Audio)
bInterfaceSubClass:   0x02 (Audio Streaming)
bInterfaceProtocol:   0x00
iInterface:           0x08
0x0409: "ITE HDMI 4K+ Bridge"
0x0409: "ITE HDMI 4K+ Bridge"
0x0409: "ITE HDMI 4K+ Bridge"

Audio Streaming Class Specific Interface Descriptor:
bLength:              0x07
bDescriptorType:      0x24
bDescriptorSubtype:   0x01
bTerminalLink:        0x09
bDelay:               0x01
wFormatTag:         0x0001 (PCM)

Audio Streaming Format Type Descriptor:
bLength:              0x0B
bDescriptorType:      0x24
bDescriptorSubtype:   0x02
bFormatType:          0x01
bNrChannels:          0x02
bSubframeSize:        0x02
bBitResolution:       0x10
bSamFreqType:         0x01
tSamFreq[1]:      0x00BB80 (48000 Hz)

Endpoint Descriptor:
bEndpointAddress:     0x81  IN
Transfer Type: Isochronous
wMaxPacketSize:     0x00C0 (192)
bInterval:            0x04

Unknown Descriptor:
bDescriptorType:      0x30
bLength:              0x06
06 30 00 00 C0 00 

Audio Streaming Class Specific Audio Data Endpoint Descriptor:
bLength:              0x07
bDescriptorType:      0x25
bDescriptorSubtype:   0x01
bmAttributes:         0x00
bLockDelayUnits:      0x00
wLockDelay:         0x0000

Interface Descriptor:
bInterfaceNumber:     0x07
bAlternateSetting:    0x00
bNumEndpoints:        0x01
bInterfaceClass:      0x03 (HID)
bInterfaceSubClass:   0x00
bInterfaceProtocol:   0x00
iInterface:           0x05
0x0409: "ITE HID Device"

HID Descriptor:
bcdHID:             0x0111
bCountryCode:         0x00
bNumDescriptors:      0x01
bDescriptorType:      0x22
wDescriptorLength:  0x0046

Endpoint Descriptor:
bEndpointAddress:     0x87  IN
Transfer Type:   Interrupt
wMaxPacketSize:     0x0200 (512)
bInterval:            0x0A

Unknown Descriptor:
bDescriptorType:      0x30
bLength:              0x06
06 30 00 00 00 04 





////////////////////////////////////////////////////////////////////////////

TWM
Tab Window Manager 

https://gitlab.freedesktop.org/xorg/app/twm.git
MIT License
https://en.wikibooks.org/wiki/Guide_to_X11/Window_Managers/twm




存儲編程
參考資料 https://www.entropywins.wtf/blog/2013/07/01/resolving-a-merge-conflict-on-gerrit/

https://www.cnblogs.com/stelite/p/8159444.html
执行hdparm命令提示HDIO_GET_IDENTITY failed的解决方法
执行 hdparm -i /dev/sda 命令，提示如下：
HDIO_DRIVE_CMD(identify) failed: Invalid exchange
HDIO_GET_IDENTITY failed: Invalid argument

通过 whatis hdparm 命令查看：
hdparm (8) - get/set SATA/IDE device parameters
可知，hdparm命令只能查看SATA/IDE设备参数，而当前是在虚拟机上安装linux系统进行测试，
查看虚拟机，得知硬盘为SCSI设备，可知是硬盘类型不匹配导致，经安装实体机进行验证，猜测
得到确认。

UTIL-LINUX
http://ftp.ntu.edu.tw/linux/utils/util-linux/v2.32/libfdisk-docs/libfdisk-Partition.html#fdisk-delete-all-partitions

https://serverfault.com/questions/250839/deleting-all-partitions-from-the-command-line
to delete the partitions in a hurry:
dd if=/dev/zero of=/dev/[disk device] bs=512 count=1

sed -e 's/\s*\([\+0-9a-zA-Z]*\).*/\1/' << EOF | fdisk ${TGTDEV}
  o # clear the in memory partition table
  n # new partition
  p # primary partition
  1 # partition number 1
    # default - start at beginning of disk 
    # default - last cylinder
  w # write the partition table
  q # and we're done
EOF

mkntfs -f -v:Avermedia ${TGTDEV}
mkexfat -f -v:Avermedia ${TGTDEV}































































a003257@vbox:~/avt/ER330/HIGV$ git diff sample/higv/avtgui/msutils.c
diff --git a/sample/higv/avtgui/msutils.c b/sample/higv/avtgui/msutils.c
index df74e87d..10690106 100755
--- a/sample/higv/avtgui/msutils.c
+++ b/sample/higv/avtgui/msutils.c
@@ -162,12 +162,42 @@ static HI_S32 playlist_new(const HI_CHAR *path, const HI_CHAR *filename)
        return HI_SUCCESS;
 }

+#define DBFILENAME "playlist.db"
+
+HI_S32 playlist_add(const HI_CHAR *currpath, const HI_CHAR *filename, const HI_CHAR *suffix, HI_U32 duration)
+{
+       HI_CHAR dbfile[MAX_LEN],
+                       pathfile[MAX_LEN]; /* currpath/filename+suffix */
+       AVM_FILE_Info info;
+       struct stat status;
+
+       sprintf(dbfile, "%s/%s", currpath, DBFILENAME);
+
+       if (suffix)
+               sprintf(pathfile, "%s/%s%s", currpath, filename, suffix);
+       else
+               sprintf(pathfile, "%s/%s", currpath, filename);
+
+       if (HI_FALSE == AVM_API_GetFileInfo(pathfile, &info)) {
+               err("Fail to get info: %s\n", pathfile);
+               return HI_FAILURE;
+       }
+
+       if (stat(pathfile, &status) < 0) {
+               err("stat %s failed\n", pathfile);
+               return HI_FAILURE;
+       }
+
+       return HI_SUCCESS;
+}
+
 /* currpath:
  *   NULL if /usr/flash/config/SystemConfig currpath equals settings.diskManage.recordPath
  *   , otherwise currpath is used.
  *
  *   duration: 0
  */
+#if 0
 HI_S32 playlist_add(const HI_CHAR *currpath, const HI_CHAR *filename, const HI_CHAR *suffix, HI_U32 duration)
 {
        HI_CHAR plist[MAX_LEN], /* currpath/.playlist */
@@ -303,6 +333,7 @@ HI_S32 playlist_add(const HI_CHAR *currpath, const HI_CHAR *filename, const HI_C

        return HI_SUCCESS;
 }
+#endif

 HI_S32 playlist_get_count(const HI_CHAR *list)
 {




a003257@vbox:~/avt/ER330/HIGV$ git diff thirdparty/Makefile
diff --git a/thirdparty/Makefile b/thirdparty/Makefile
index 29b7aed1..7b87a9a2 100755
--- a/thirdparty/Makefile
+++ b/thirdparty/Makefile
@@ -16,7 +16,7 @@ CUNIT_DIR := c-unit
 #===============================================================================
 .PHONY : all clean install uninstall
 #tiff compile rely on jpeg
-exclude_softwares += c-unit avernetmgr rp-pppoe libssl
+exclude_softwares += c-unit avernetmgr rp-pppoe libssl sqlite
 softwares := $(shell find . -maxdepth 1 -type d)
 softwares := $(basename $(patsubst ./%,%,$(softwares)))
 softwares := $(filter-out $(exclude_softwares), $(softwares))



#####################################################################

/usr/flash/config/SystemConfig

settings/enterWizard: true false

wa_set_bool_to_json(FN_SYSTEM_CONFIG_JSON_NAME, "settings.



#####################################################################



mount -t ntfs /dev/ada1 /mnt
三小時架好 FreeNAS 私有雲
http://chiutienyu.blogspot.com/2017/05/freenas_9.html

For adding NFS share on FreeNAS goto: Sharing -> Unix (NFS) -> Add Unix (NFS) Share



FreeNAS 11.3 requires a 64-bit CPU and a minimum of 8GB RAM
DIY FreeNAS 超私有雲架設之術 https://www.computerdiy.com.tw/diy-free-nas/

create table if not exists playlist(id INTEGER PRIMARY KEY, name TEXT, thumb TEXT, type INTEGER, vdofmt INTEGER, duration INTEGER, size INTEGER, lmtime INTEGER, quality INTEGER, vdostd INTEGER, width INTEGER, height INTEGER);

insert into playlist (name, thumb, type, vdofmt, duration, size, lmtime, quality, vdostd, width, height) VALUES ("20201012-165501-H264-00.mp4", ".thumb/20201012-165501-H264-00_thumb.jpg", 0, 0, 60, 178276199, 1602492962, 1, 10, 1920, 1080);

select count(*) from PLAYLIST



什麼是SQLite？

SQL是 structured query language的縮寫，特殊設計的程式語言，用於資料庫查詢。

SQLite最早是由Richard Hipp於2000年開發。Hipp是Duke大學的博士。

SQLite是 in-process 函式庫，不會自行開啟行程，就在應用程序的行程中執行。
Serverless，非server-client架構，無須一個server行程才能執行。
Self-contained，可譯為自包涵，不相依其他函式庫。
Zero-configuration，無須麻煩地撰寫或調整配置檔。
Transactional，符合ACID原則：atomic, consistent, isolated, durable，所以應用程序死翹翹、作業系統死翹翹、或斷電不會影響資料傳輸。

適合嵌入式開發：
跨平台，不拘 Windows/Linux、32/64-bit、little/big endian。不過 8-bit microcontroller效能有限，也許會跑不動。
所有資料都在一個檔案裡面，檔案可包含多張tables, indices, triggers, and views。
Native UTF-8，所以在 Linux 上取出字串，無須轉換即可使用。
沒有 license 的問題。
可以控制在哪種記憶體創建 tables。

可應用在手機、PDA、MP3等等：電話聯絡簿可以是一個資料庫；MP3的播放清單可以是一個資料庫。最後的參考資料有一本書 The definitive guide to SQLite 第二版最後兩章，即介紹如何在 iOS、Android 上使用SQLite寫程式。

#include <sqlite3.h>
API
sqlite3_open(), sqlite3_close()
sqlite3_exec()
SQLite syntax
-lsqlite3

SQLite syntax

官網 www.sqlite.org 

CREATE TABLE IF NOT EXISTS sch(id INTEGER PRIMARY KEY, start INTEGER, end INTEGER, freq INTEGER, ch INTEGER);
CREATE INDEX IF NOT EXISTS idx_tsk_start ON tsk(start);
SELECT * FROM tsk WHERE NOT ((%d < start) OR (end < %d));
INSERT INTO tsk(start, end, freq, ch, schid) VALUES (%d, %d, %d, %d, %d);

Syntax Diagrams For SQLite https://sqlite.org/syntaxdiagrams.htmldiff --git a/media_adpt/hi3516cv500/sdk b/media_adpt/hi3516cv500/sdk
index 378a739d..744b1af5 120000
--- a/media_adpt/hi3516cv500/sdk
+++ b/media_adpt/hi3516cv500/sdk
@@ -1 +1 @@
-/home/dave/project/HI/ER330/HIGV/media_adpt/hi3516cv500/../../../sdk
\ No newline at end of file
+/home/a003257/avt/ER330/HIGV/media_adpt/hi3516cv500/../../../sdk
\ No newline at end of file
diff --git a/sample/higv/avtgui/Makefile b/sample/higv/avtgui/Makefile
index 0ab198c7..d3021aa6 100755
--- a/sample/higv/avtgui/Makefile
+++ b/sample/higv/avtgui/Makefile
@@ -45,11 +45,13 @@ CXXFLAGS += -I $(GST_DIR_INCLUDE)/include/
 CXXFLAGS += -I $(GST_DIR_INCLUDE)/include/curl/
 CXXFLAGS += -I $(GST_DIR_INCLUDE)/include/libxml2
 CXXFLAGS += -I $(THIRDPARTY)/json-c/json-c-0.13/
+CXXFLAGS += -I $(THIRDPARTY)/sqlite/sqlite-autoconf-3330000/
 
 LDFLAGS += -L../../../thirdparty/avtconfig
 LDFLAGS += -L../../../thirdparty/avernetmgr
 LDFLAGS += -L $(GST_DIR_INCLUDE)/lib -lcurl -lssl -lcrypto -lz -lpng
 LDFLAGS += -L $(THIRDPARTY)/json-c/json-c-0.13/.libs -ljson-c
+LDFLAGS += -L $(THIRDPARTY)/sqlite/sqlite-autoconf-3330000/.libs -lsqlite3
 #LDFLAGS += -L $(MPP_SAMPLE)/avt_ugmcu  libugmcu.a 
 LDFLAGS += -L $(MPP_SAMPLE)/../lib
 LDFLAGS += -lrt
diff --git a/sample/higv/avtgui/builder/xml/datamodel/datamodel.xml b/sample/higv/avtgui/builder/xml/datamodel/datamodel.xml
index 5371d9ba..7836e1c4 100755
--- a/sample/higv/avtgui/builder/xml/datamodel/datamodel.xml
+++ b/sample/higv/avtgui/builder/xml/datamodel/datamodel.xml
@@ -37,6 +37,15 @@
     registerdatachange=""
     unregisterdatachange="" />
 
+<datamodel
+    id="ADM_MSTUDIO_V2"
+    field="SICO:resid:4;LICO:string:256;TYPE:u32:4;NAME:string:128;HEIGHT:u32:4;VDOSTD:u32:4;VDOFMT:u32:4"
+    datasource="userdb"
+    getrowcount="mstudio_v2_getrowcount"
+    getrowvalue="mstudio_v2_getrowvalue"
+    registerdatachange="mstudio_v2_registerdatachange"
+    unregisterdatachange="mstudio_v2_unregisterdatachange" />
+
 <datamodel
     id="ADM_MSTUDIO_SETDSK"
     field="ICON:resid:4;TYPE:u32:4;DESC:string:128;DEVNODE:string:128"
diff --git a/sample/higv/avtgui/msutils.c b/sample/higv/avtgui/msutils.c
index df74e87d..10690106 100755
--- a/sample/higv/avtgui/msutils.c
+++ b/sample/higv/avtgui/msutils.c
@@ -162,12 +162,42 @@ static HI_S32 playlist_new(const HI_CHAR *path, const HI_CHAR *filename)
 	return HI_SUCCESS;
 }
 
+#define DBFILENAME "playlist.db"
+
+HI_S32 playlist_add(const HI_CHAR *currpath, const HI_CHAR *filename, const HI_CHAR *suffix, HI_U32 duration)
+{
+	HI_CHAR dbfile[MAX_LEN],
+			pathfile[MAX_LEN]; /* currpath/filename+suffix */
+	AVM_FILE_Info info;
+	struct stat status;
+	
+	sprintf(dbfile, "%s/%s", currpath, DBFILENAME);
+
+	if (suffix)
+		sprintf(pathfile, "%s/%s%s", currpath, filename, suffix);
+	else
+		sprintf(pathfile, "%s/%s", currpath, filename);
+
+	if (HI_FALSE == AVM_API_GetFileInfo(pathfile, &info)) {
+		err("Fail to get info: %s\n", pathfile);
+		return HI_FAILURE;
+	}
+
+	if (stat(pathfile, &status) < 0) {
+		err("stat %s failed\n", pathfile);
+		return HI_FAILURE;
+	}
+
+	return HI_SUCCESS;
+}
+
 /* currpath: 
  *   NULL if /usr/flash/config/SystemConfig currpath equals settings.diskManage.recordPath
  *   , otherwise currpath is used.
  *
  *   duration: 0
  */
+#if 0
 HI_S32 playlist_add(const HI_CHAR *currpath, const HI_CHAR *filename, const HI_CHAR *suffix, HI_U32 duration)
 {
 	HI_CHAR plist[MAX_LEN], /* currpath/.playlist */
@@ -303,6 +333,7 @@ HI_S32 playlist_add(const HI_CHAR *currpath, const HI_CHAR *filename, const HI_C
 
 	return HI_SUCCESS;
 }
+#endif
 
 HI_S32 playlist_get_count(const HI_CHAR *list)
 {
diff --git a/thirdparty/Makefile b/thirdparty/Makefile
index 29b7aed1..7b87a9a2 100755
--- a/thirdparty/Makefile
+++ b/thirdparty/Makefile
@@ -16,7 +16,7 @@ CUNIT_DIR := c-unit
 #===============================================================================
 .PHONY : all clean install uninstall
 #tiff compile rely on jpeg
-exclude_softwares += c-unit avernetmgr rp-pppoe libssl
+exclude_softwares += c-unit avernetmgr rp-pppoe libssl sqlite
 softwares := $(shell find . -maxdepth 1 -type d)
 softwares := $(basename $(patsubst ./%,%,$(softwares)))
 softwares := $(filter-out $(exclude_softwares), $(softwares))
 
 `````````````````````````````````````````````````````````````````````
