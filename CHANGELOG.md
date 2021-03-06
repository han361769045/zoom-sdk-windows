# CHANGELOG

## 2018-05-22
### Added
1.c++ sdk
a> Configuration of Meeting Service Interface

support to config DSCP for audio video session

support to redirect click event of participant list button

support to disable copy and paste feature when remote control

support to disable UI elements of split screen mode

support to auto hide join audio dialog when it shown

support to enable hide the full phone number for pure call in user
b> H323 helper interface

support to get h323 device for current meeting

change the CallOutH323 interface

c> Sharing of Meeting Service Interface

support to block window form screen share without change windows's style

d>Meeting Service Interface

support to get meeting connect type

e> Setting Service Interface

support to enable or disable auto enter full screen video mode when view share

support to enable or disable always show name on video

support to enable or disable turn off video when join meeting

support to enable or disable original input of mic

support to enable or disable stereo audio

add new interface for statistic setting

f>L10n

add new language support(Italian Portuguese Russian)

2.c# sdk

add new c++ interface wrap

## 2017-12-25
### Added

1.c++ sdk
    a> setting service

add SettingTabPage option in ShowSettingDlgParam

add EnableHDVideo and IsHDVideoEnabled interface in IVideoSettingContext

b> meeting service

add IsMeetingLocked interface in IMeetingService

rename GetMeetingConnQuality to GetSharingConnQuality in IMeetingService

support to get sending and receiving connection quality of audio/video/share session

b> meeting audio controller

fix onUserActiveAudioChange does not worked bugs in IMeetingAudioCtrlEvent

c>meeting configuration

add RedirectClickEndMeetingBTNEvent interface in IMeetingConfiguration

add EnableClaimHostFeature interface in IMeetingConfiguration

d> meeting share controller

add ShowSharingAppSelectWnd interface in IMeetingShareController

add share computer sound interface

IsSupportEnableShareComputerSound

EnableShareComputerSound

add optimize for full screen video clip interface:

IsSupportEnableOptimizeForFullScreenVideoClip

EnableOptimizeForFullScreenVideoClip

e>meeting ui controller

add onEndMeetingBtnClicked callback event in IMeetingUIControllerEvent

2.c# sdk

a>wrap new c++ interface and callback event

b>fix callback event does not worked issue


## 2017-11-01

### Added

1.add two new callback events in IMeetingServiceEvent

a>onMeetingStatisticsWarningNotification :  Meeting statistics warning notification callback

b>onMeetingSecureKeyNotification : Meeting secure key notification, need to web backend and special account type support.

2.fix crash bug of sdk cleanup

3.minor bug fix

## 2017-10-10

### Added

01.Interface refactoring

for details, please visit: https://developer.zoom.us/docs/windows/windows-sdk-refactor-details/

02.New interface of change inmeeting display user name and notification of inmeeting display user name changed

03.New interface of hide/show sharing frame window

04.Notification of active speaker

05.Support L10N customized

06.Notification of current sharing type

07.New interface of get current meeting id

08.New interface of hide video thumnails

09.New interface of pre-populate register email and user name when join webinar

10.Support select sharing app window customized

11.Notification of meeting ui action

12.New interface of change the main window to no video mode.

13.Notification of proxy detect complete

14.New interface of get call-in number list

15.Add more interface to get user information

16.Add more interface of meeting settings

17.New interface of split screen mode

18.New interface of schedule/edit meeting dialog, same as zoom windows client.

19.Support Airhost dialog customized

20.bug fix

## 2017-06-08

### Added

1. Lock share status notify

2. Support switch video wall to next page feature

3. Support join leave VoIP feature

4. Support get meeting type feature

5. Support get user role feature

6. Breakout room feature enhancement

7. Webinar feature enhancement

8. Waiting room feature enhancement

9. More settings support:
    1> Support disable input meeting password dialog
    2> Allow or disallow "can unmute by self if mute by host" flag
    3> Support hide enter and exit full screen button

10. Bug fix

## 2017-04-12

### Added

1. Webinar promote and depromote meeting status change notify

2. Join and leave Breakout room meeting status change notify

3. Show or hide invite button in meeting ui and callback invite button click message support

4. Add new interface for H323 password

5. Bug Fix

## 2017-03-10

### Added

1. Add host change callback

2. Add spotlight video change callback

3. Add self record privilige change callback

4. Add Low Or Raise Hand Status change callback

5. Bug Fix

## 2017-03-02

### Added

1. Enhancement of proxy
   zoom_sdk.h
    - New interface:
		SDK_API SDKError CreateNetworkConnectionHelper(INetworkConnectio Helper** ppNetworkHelper);
        network_connection_handler_interface.h
    - New callback event:
        virtual void onProxySettingNotification(IProxySettingHandler* handler) = 0;

2. Enhancement of SSL cert Verification
   zoom_sdk.h
    - New interface:
    	SDK_API SDKError CreateNetworkConnectionHelper(INetworkConnectionHelper** ppNetworkHelper);
    	network_connection_handler_interface.h
    - New callback event:
    	virtual void onSSLCertVerifyNotification(ISSLCertVerificationHandler* handler    ) = 0;

3. Video/Audio session connection quality API
    meeting_service_interface.h
    - New interface:
       virtual ConnectionQuality GetAudioConnQuality() = 0;
       virtual ConnectionQuality GetVideoConnQuality() = 0;

4. Bugs fix

## 2017-02-10

### Added

1. Support waiting room

2. Support embedded browser feature

3. Refine the sdk demo project, add VS2015 support

5. Bug Fix

## 2017-01-20

### Added

1. Support to join Webinar meeting with as Panelist Support to pin/spotlight video

2. Support to pause/resume screen sharing Support H.323/SIP callout directly

3. Support invite by Phone andCall Medirectly

4. Add watermark - Powered by Zoom 

5. Support to start/join meeting without audio

6. Support to start/join meeting without video

7. Support Multi-share

8. New interface in ISettingService

9. New interface in IMeetingConfiguration 

10. Refine IMeetingService interface

## 2016-11-15

### Added

1. Add new interface for get windows handle

2. Fix branding issue in setting dialog, whiteboard and airhost window

3. Fix participant id don't take effect when start/join meeting

## 2016-10-05

### Added

1. fix leave meeting wnd cut off issue

## 2016-06-05

### Added

1. Support login zoom user
