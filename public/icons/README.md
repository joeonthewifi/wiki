# Icon Setup

## Where to Place Your Icons

Place your Minecraft skull PNG in this directory:

```
public/icons/minecraft-skull.png
```

### Icon Requirements
- **Format**: PNG with transparency recommended
- **Size**: 64x64px or higher (will be scaled to 20x20 in the UI)
- **File name**: `minecraft-skull.png` (exactly as shown)

### Current Icon Setup

The navigation uses these icons:

1. **ImHer0** (Main section): `minecraft-skull.png` (your custom icon)
2. **Wither's Wrath**: Lucide "Skull" icon (built-in)
3. **Upcoming Pack**: Lucide "PackageOpen" icon (built-in)

### Adding More Custom Icons

If you want to add more custom icons for other sections:

1. Add the PNG file to `public/icons/`
2. Update `src/lib/source.ts` to add the new icon to `customIcons`
3. Reference it in the appropriate `meta.json` file

Example:
```typescript
CustomIconName: (props: any) => (
  <Image
    src="/icons/your-icon.png"
    alt="Description"
    width={20}
    height={20}
    {...props}
  />
),
```

Then use `"icon": "CustomIconName"` in your `meta.json`.
