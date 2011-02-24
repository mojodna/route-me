default:
	xcodebuild -target "MapView framework" -configuration ${CONFIGURATION} -sdk iphoneos build
	xcodebuild -target "MapView framework" -configuration ${CONFIGURATION} -sdk iphonesimulator build
	cp -R build/${CONFIGURATION}-iphonesimulator build/${CONFIGURATION}-universal
	-lipo -create build/${CONFIGURATION}-iphoneos/MapView.framework/MapView build/${CONFIGURATION}-iphonesimulator/MapView.framework/MapView -output build/${CONFIGURATION}-universal/MapView.framework/MapView

clean:
	-rm -rf build
