
clean
---
xcodebuild clean -workspace ExampleProject.xcworkspace -scheme ExampleProject

build
---
xcodebuild build -workspace ExampleProject.xcworkspace -scheme ExampleProject


archive
---
xcodebuild archive -workspace ExampleProject.xcworkspace -scheme ExampleProject -archivePath ./build/example_project.xcarchive


export
---
xcodebuild -exportArchive -archivePath ./build/example_project.xcarchive -exportPath ./build -exportOptionsPlist ./export-options.plist -allowProvisioningUpdates

