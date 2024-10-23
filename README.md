# TPFanControl for dual-fan ThinkPads

Confirmed to be working on:
- ThinkPad P52
- should work on other dual fan Thinkpads

## About

This is a fork of https://github.com/nikolasgd/TPFanControl-dual-fan.

Features / fixes in this release:

- no or very rarely reported errors from EC (Thinkpad P52)
- 100% fix of any fan persist active after achiving Level 0 (where fans should be stopped)

## Installation

Either install [tvicport](https://www.entechtaiwan.com/dev/port/index.shtm) manually or install the original version of TPFanControl found [here](https://thinkwiki.de/TPFanControl) and run the dual-fan version instead of the original version:

After you installed the original version of TPFanControl, replace the TPFanControl.exe (and possibly TPFanControl.ini) with the files from the release package or the corresponding files in the `fancontrol/Release` directory.

## Running at startup
To my knowledge, running at startup is currently not possible with Windows 10 because it lacks a certificate to prevent the Windows security warning.

You can however achieve the same result with Windows Task Scheduler:
- Create a new task, give it a descriptive name and select "Run with highest privileges"
- In tab "Triggers" create a new trigeger and select "Begin task": "At log on"
- In tab "Actions", create a new action and select "Start a program" and the path to TPFanControl.exe
- Enjoy :)
