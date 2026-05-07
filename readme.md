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
- [PreviewRenderUtility.AddSingleGO](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.AddSingleGO)
- [PreviewRenderUtility.BeginPreview](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.BeginPreview)
- [PreviewRenderUtility.BeginStaticPreview](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.BeginStaticPreview)
- [PreviewRenderUtility.camera](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.camera)
- [PreviewRenderUtility.cameraFieldOfView](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.cameraFieldOfView)
- [PreviewRenderUtility.Cleanup](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.Cleanup)
- [PreviewRenderUtility.Constructor](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.Constructor)
- [PreviewRenderUtility.CreateLight](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.CreateLight)
- [PreviewRenderUtility.EndAndDrawPreview](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.EndAndDrawPreview)
- [PreviewRenderUtility.EndPreview](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.EndPreview)
- [PreviewRenderUtility.EndStaticPreview](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.EndStaticPreview)
- [PreviewRenderUtility.lights](https://github.com/CyberFoxHax/Unity3D_PreviewRenderUtility_Documentation/wiki/PreviewRenderUtility.lights)

### Quick Start

```csharp
PreviewRenderUtility preview = new PreviewRenderUtility();
preview.BeginPreview(rect, GUIStyle.none);
// ... setup camera, lights, AddSingleGO(), DrawMesh() etc.
Texture result = preview.EndPreview();
preview.Cleanup();
```

### Important Notes
- Always call `Cleanup()` (especially in `OnDisable`).
- One instance reused is better than creating many.
- Works in Editor only (`UnityEditor` namespace).

### Contributing
Feel free to open **Issues** or **Pull Requests** to improve the documentation. Corrections, new examples, version-specific notes, etc. are very welcome.

---

**Made because Unity Technologies won't document it.**
