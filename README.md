# Buckbone
A simple android project generator for the Buck build system.

## Install

	sudo wget https://raw.githubusercontent.com/zserge/buckbone/master/buckbonejava -O /usr/local/bin
	sudo chmod +x /usr/local/bin/buckbonejava

## Usage

	buckbone com.example.myapp /path/to/app
	cd /path/to/app
	buck build app

Sources would be localed at /path/to/app/java/com/example/myapp.
Android resources would be located at /path/to/app/res/com/example/myapp/res.

## Generated java project structure

	# Top-level Buck configuration
	./.buckconfig

	# Application configuration
	./apps/com.example.buck/BUCK
	./apps/com.example.buck/debug.keystore
	./apps/com.example.buck/debug.keystore.properties
	./apps/com.example.buck/AndroidManifest.xml
	./apps/DEFS

	# Java code
	./java/com/example/buck/BUCK
	./java/com/example/buck/MainActivity.java

	# Android resources and assets
	./res
	./res/AndroidManifest.xml
	./res/com/example/buck/BUCK
	./res/com/example/buck/res/values/strings.xml
	./res/com/example/buck/assets

## Kotlin

There is also a buckbonekotlin to generate the Buck skeleton for the android
app written in Kotlin, but it's experimental.

Usage:

	./buckbonekotlin com.example.myapp /path/to/app /path/to/kotlinc
