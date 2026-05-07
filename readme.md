# PreviewRenderUtility Documentation

> Community documentation for Unity's undocumented `PreviewRenderUtility` class.

**Unity still hasn't documented this extremely useful Editor class.** This repo exists to fix that.

![PreviewRenderUtility example](https://raw.githubusercontent.com/wiki/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/RenderCubeExample.png)

### What is PreviewRenderUtility?

`PreviewRenderUtility` lets you render objects (meshes, prefabs, particles, etc.) into textures or directly into Editor GUI with full control over lighting, camera, and scene setup. It's the same system Unity uses internally for asset previews.

### 📖 Documentation

→ **[Full Documentation in the Wiki →](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility)**

Key pages:
- [PreviewRenderUtility](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility)
- (Add more pages as you create them)

### Quick Start

```csharp
PreviewRenderUtility preview = new PreviewRenderUtility();
preview.BeginPreview(rect, GUIStyle.none);
// ... setup camera, lights, AddSingleGO(), DrawMesh() etc.
Texture result = preview.EndPreview();
preview.Cleanup();
```
