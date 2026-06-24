<h1>Instance Manipulation</h1>

---

<div class="sym-block sym-function" data-name="XPLMInstanceSetPosition" data-type="function" markdown="1">

## XPLMInstanceSetPosition { .symbol-title }

<span class="sym-badge badge-fn">function</span>

Updates both the position of the instance and all datarefs you registered for it.  Call this from a flight loop callback or UI callback.

__DO_NOT__ call XPLMInstanceSetPosition from a drawing callback; the whole point of instancing is that you do not need any drawing callbacks.
Setting instance data from a drawing callback may have undefined consequences, and the drawing callback hurts FPS unnecessarily.

The memory pointed to by the data pointer must be large enough to hold one float for every dataref you have registered, and must contain valid
floating point data.

BUG: before X-Plane 11.50, if you have no dataref registered, you must still pass a valid pointer for data and not null.

```cpp
XPLM_API void       XPLMInstanceSetPosition(
                         XPLMInstanceRef      instance,
                         const XPLMDrawInfo_t * new_position,
                         const float *        data
                    );
```

</div>

---

<div class="sym-block sym-function" data-name="XPLMInstanceSetPositionDouble" data-type="function" markdown="1">

## XPLMInstanceSetPositionDouble { .symbol-title }

<span class="sym-badge badge-fn">function</span> <span class="sym-badge badge-version">XPLM420</span>

Updates both the position of the instance and all datarefs you registered for it.  Call this from a flight loop callback or UI callback.

__DO_NOT__ call XPLMInstanceSetPositionDouble from a drawing callback; the whole point of instancing is that you do not need any drawing
callbacks. Setting instance data from a drawing callback may have undefined consequences, and the drawing callback hurts FPS unnecessarily.

The memory pointed to by the data pointer must be large enough to hold one float for every dataref you have registered, and must contain valid
floating point data.

```cpp
XPLM_API void       XPLMInstanceSetPositionDouble(
                         XPLMInstanceRef      instance,
                         const XPLMDrawInfoDouble_t * new_position,
                         const float *        data
                    );
```

</div>

---



<!-- whitespace for navigation purposes -->
<div style="height:100vh;"></div>