# WIP

# Build everything once, serialize test execution

tuist test

# Build everything once, parallelize test execution
// Needs a new scheme that includes all tests, friggin tuist

xcodebuild build-for-testing -scheme GlobalTests -destination 'platform=iOS Simulator,name=iPhone 8 Plus,OS=14.4' -showBuildTimingSummary | xcpretty

xcodebuild test-without-building -scheme ExampleProjectTests -destination 'platform=iOS Simulator,name=iPhone 8 Plus,OS=14.4' | xcpretty

xcodebuild test-without-building -scheme ExampleProjectKitTests -destination 'platform=iOS Simulator,name=iPhone 8 Plus,OS=14.4' | xcpretty

xcodebuild test-without-building -scheme ExampleProjectUITests -destination 'platform=iOS Simulator,name=iPhone 8 Plus,OS=14.4' | xcpretty

# Build each framework in isolation
xcodebuild test -scheme ExampleProjectTests -destination 'platform=iOS Simulator,name=iPhone 8 Plus,OS=14.4' | xcpretty

xcodebuild test -scheme ExampleProjectKitTests -destination 'platform=iOS Simulator,name=iPhone 8 Plus,OS=14.4' | xcpretty

xcodebuild test -scheme ExampleProjectUITests -destination 'platform=iOS Simulator,name=iPhone 8 Plus,OS=14.4' | xcpretty
