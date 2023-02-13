# Avoiding_Mocking_UserDefaults

```swift
class LoginTests: XCTestCase {
    private var userDefaults: UserDefaults!
    private var manager: LoginManager!
    
    override func setUp() {
        super.setup()
        
        userDefaults = UserDefaults(suiteName: #file)
        userDefaults.removePersistentDomain(forName: #file)
        
        manager = LoginManager(userDefaults: userDefaults)
    }
}
```
