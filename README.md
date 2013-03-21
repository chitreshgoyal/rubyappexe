Rubyappexe
==========

gem install ocra

Innosetup

    install innosetup from http://www.jrsoftware.org/isdl.php

    add innopath directory {example: D:\Inno Setup 5;}


D:\wxruby\bin;



mobileapp.iss

    ; -- Example1.iss --
    ; Demonstrates copying 3 files and creating an icon.
    
    ; SEE THE DOCUMENTATION FOR DETAILS ON CREATING .ISS SCRIPT FILES!
    
    [Setup]
    AppName=mobileapp
    AppVersion=1.0
    DefaultDirName={pf}\mobileapp
    DefaultGroupName=mobileapp
    UninstallDisplayIcon={app}\mobileapp.exe
    Compression=lzma2
    SolidCompression=yes
    OutputDir=userdocs:Inno Setup Examples Output
    OutputBaseFilename=mobileappInstaller
    
    [Icons]
    Name: "{group}\mobileapp"; Filename: "{app}\mobileapp.exe"
    Name: "{group}\Uninstall mobileapp"; Filename: "{uninstallexe}"


ocra mobileapp/script/rails mobileapp --output mobileapp.exe --add-all-core --gemfile mobileapp/Gemfile --no-dep-run --chdir-first --no-lzma --

innosetup mobileapp.iss -- server
