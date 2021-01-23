@echo off

if not "%1"=="am_admin" (powershell start -verb runas '%0' am_admin & exit /b)
net stop audiosrv
net stop AudioEndpointBuilder
net start AudioEndpointBuilder
net start audiosrv
EXIT
