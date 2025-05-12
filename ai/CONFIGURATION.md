### 🧱 Code Structure & Modularity
- **Limit each file to 500 lines.** If you approach this limit, refactor by splitting into modules or helper files.
- **Group code by feature or responsibility**, keeping modules self-contained.
- **Use clear, consistent imports**, preferring relative imports within the same package.

### 📎 Style & Conventions
- **Language**: Kotlin (Kotlin Multiplatform for shared code).
- **Naming & Formatting**: Follow standard Kotlin conventions (e.g. `camelCase` for functions, `PascalCase` for types).
- **Documentation**:  
  - Public APIs must have KDoc comments.  
  - Avoid excessive inline comments; reserve them for non-obvious logic.

### 📚 Documentation & Clarity
- **Comment only non-obvious code** to aid a mid-level developer’s understanding.
- For complex algorithms, add a brief inline note explaining *why*, not just *what*.
- **Generate user-friendly docs** with Dokka from KDoc.

### 🧪 Testing & Reliability
- **Unit tests** are required for every new feature.
- **Update existing tests** whenever related logic changes.
- **Test cases** must include:  
  1. One “happy path” test  
  2. One edge-case test  
  3. One failure-case test  
- **Multiplatform coverage**: Run tests on JVM, JS, and Native targets.
- **Mocking**: Use MockK KMP.
- **Optional**: Add integration and UI tests where applicable.

### ⚙️ Build System
- **Gradle** is the standard build tool.

### 🌲 Version Control
- **Git workflow**:  
  - `main` = production  
  - `dev` = integration  
  - `feature/*` = individual features

### 🔐 Configuration Management
- Store secrets (API keys, DB URLs) in `.env`; never commit actual `.env` files.
- Include a `.env.example` listing all required variables.
