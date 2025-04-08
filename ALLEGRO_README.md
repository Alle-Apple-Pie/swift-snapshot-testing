# We need some fixes in our codebase

We probably should do bigger refactor and treat this library as swift-testing adapter instead of using it directly in codebase, but it is how it is and while
updating swift-version version you have to:
1. Be sure to add [delay method](https://github.com/allegro-internal/buyers-app-ios/pull/14344/files), based on: https://github.com/pointfreeco/swift-snapshot-testing/pull/742
2. Add fix for [UIWindow](https://github.com/Alle-Apple-Pie/swift-snapshot-testing/commit/958b7d5bb51440fa5bfd9d7e4aeff9e5213d4da3), based on: https://github.com/pointfreeco/swift-snapshot-testing/pull/366
3. Make sure [subpixelThreshold was removed from the codebase](https://github.com/Alle-Apple-Pie/swift-snapshot-testing/commit/2152e0947997945cadc797f3374fbece0cef93ad)
4. Remove deprecations of `assertSnapshot` methods. 
