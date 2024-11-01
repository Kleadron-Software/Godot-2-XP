## GDXP 2.2 dev1

#### General
- Renamed to GDXP 2.2
- VU meter added back to top right since there's enough space.
- Added gizmo for concave collision shapes.
- RoomInstance node and Room resource have been named back to their original names. (from Room and RoomBounds)
- Fixed chibi tracker module player's panning so your left ear can also enjoy the music.
- Backported sync_via_compositor from Godot 3. It's on by default now.
- Removed artificial delay from low processor mode since it made the editor feel awful to use.
- Backported the frame delay code from Godot 3 because the above would spinwait on low procesor mode... :)
- Fixed the editor gizmo for directional lights layering up every time you clicked it, becoming brighter each time.
- Updated copyright statements and authors file.

## Godot 2.1.7 RC interim version

This does not track individual bugfixes and changes made to Godot XP's new features since this section.

#### General
- Compiles with VS2010.
- NO_THREADS defined since NT 5.1 lacks the InterlockedCompareExchange64 function.
- WASAPI audio driver disabled by default since it doesn't work for XP.
- Windows 8/10 logo for Windows export replaced with Windows XP logo to reflect supported platform.
- DEBUG_MEMORY_ENABLED disabled since it was causing crashes, and I have no idea why.
- Various changes to UI to make it more space efficient by default.
- GUI theme is based on Godot 1.0's but as gray with green accents.
- VU meter disabled for space reasons.

#### Rendering
- GLES1 rasterizer added with support for most features except shaders and render targets.
- Billboard and Billboard Y properly implemented for both GLES1 and GLES2 rasterizers.
- Display driver project setting is now a dropdown option instead of a text box.
- Mipmap filtering options adjusted so mipmaps render more predictably to the filtering setting. They at least look better to me.
- Material/Scene previews are now allowed to fail (viewport capture has since been added, so this is unecessary).
- FixedMaterial specular exponent maximum changed to 128.

#### Backports
- Version tag on the bottom panel backported from Godot 3.
- Nodes that have attached script functions like `_process` will now automatically set process to true, like in Godot 3+.
- GUI Controls now scale properly when rotated like in Godot 3+.
