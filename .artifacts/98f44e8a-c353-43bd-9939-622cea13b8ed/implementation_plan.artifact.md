# Fix Compilation Error: Unresolved R reference

The user is encountering a compilation error in `MainActivity.kt` because the `R` class (Android resources) cannot be resolved. This is due to a mismatch between the package declared in the file (`com.example.assignment`) and the project's namespace (`com.example.myapplication2`).

## Proposed Changes

### app module

#### [MODIFY] [MainActivity.kt](file:///D:/CODE/Android/app/src/main/java/com/example/myapplication2/MainActivity.kt)
- Update the package declaration from `com.example.assignment` to `com.example.myapplication2`.
- This will align the class with its directory structure and allow it to automatically resolve the generated `R` class.

## Verification Plan

### Automated Tests
- Run `./gradlew :app:compileDebugKotlin` to verify that the compilation error is resolved.
