## Installation
# Adding a DLL Reference - Detailed Steps

## Downloading from GitHub
To get the DLL package from the repository:
1. Navigate to [https://github.com/CoderKinley/Side-Menu-Panel-Library](https://github.com/CoderKinley/Side-Menu-Panel-Library)
2. Download the Zipfile including `Lib` and `LeftMenuPanel.dll`

### Step 1: Organize Your Library Files
1. Create a dedicated folder in your project (recommended):
   * Right-click on your project in Solution Explorer
   * Select `Add` → `New Folder`
   * Name it `lib`, `references`, or `external-libs`
   * Copy the `.dll` file into this folder

### Step 2: Add the DLL Reference
#### Method A: Using Solution Explorer
1. Right-click on the `References` or `Dependencies` node in your project
2. Select `Add Reference...`
3. In the Reference Manager dialog:
   * Select the `Browse` tab
   * Click the `Browse...` button
   * Navigate to the folder where you placed the DLL
   * Select the DLL file and click `OK`
   * Ensure the reference is checked in the list
   * Click `OK` to confirm

#### Method B: Using Project Properties
1. Right-click on your project in Solution Explorer
2. Select `Properties`
3. Go to the `References` tab (or `Dependencies` in newer versions)
4. Click `Add` or `Add Reference...`
5. Follow the same browsing steps as Method A

### Step 3: Set Reference Properties (Optional but Recommended)
After adding the reference, you can modify its properties:
1. Click on the newly added reference in Solution Explorer
2. In the Properties window (F4):
   * Set `Copy Local` to `True` (ensures the DLL is copied to your output directory)
   * Verify that `Specific Version` is set appropriately for your needs

### Step 4: Using the Library in Code
1. Add the required namespace at the top of your code files:
   ```csharp
   using LeftMenuPanelLibrary;  // The namespace for the Side Menu Panel Library
   ```
2. If you're unsure about the namespace:
   * Use Object Browser (View → Object Browser) to explore the DLL
   * Or try an IDE like JetBrains dotPeek to inspect the DLL contents

### Step 5: Check Build Configuration
1. Make sure the DLL is compatible with your project's target framework
2. For platform-specific DLLs, ensure your project's platform target matches (x86, x64, or Any CPU)
3. Build your project to verify the reference is working correctly

### Troubleshooting Common Issues
- **"Could not load file or assembly..."** error: Ensure the DLL and all its dependencies are accessible
- **Missing dependencies**: Some DLLs require additional libraries; check documentation
- **Version conflicts**: Make sure the DLL version is compatible with your .NET version
- **Reference not working**: Try restarting Visual Studio after adding references
