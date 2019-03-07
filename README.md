# sdrsharp  SMP Debian 4.19.16-1 (2019-01-17) x86_64 GNU/Linux

apt install mono-complete libportaudio2 librtlsdr0 librtlsdr-dev

cd sdrsharp
xbuild /p:TargetFrameworkVersion="v4.5" /p:Configuration=Release

cd Release
ln -s /usr/lib/x86_64-linux-gnu/libportaudio.so.2 libportaudio.so
ln -s /usr/lib/x86_64-linux-gnu/librtlsdr.so.0 librtlsdr.dll

mono SDRSharp.exe
