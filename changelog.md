#### 1.0.1 (2024-12-28)

LoadAddOn and IsAddOnLoaded were giving errors, changed to the following.

There seemed to be an issue on load in Core.lua debug line 7
```
if debug and LoadAddOn then
    LoadAddOn("Blizzard_DebugTools")
    LoadAddOn("LibDebug")
    if LibDebug then
        LibDebug()
    end
end
```

There seemed to be an issue on load in TransmogCleanup.lua line 716:

```
if IsAddOnLoaded and IsAddOnLoaded("GnomishVendorShrinker") then
    fixPosition = true
    fixFramelevel = true
end

if IsAddOnLoaded and IsAddOnLoaded("ElvUI_SLE") then --ElvUI plugin Shadow and Light
    fixPosition = true
    fixFramelevel = true
end
```