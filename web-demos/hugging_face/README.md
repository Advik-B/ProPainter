# ProPainter Web Demo User Guide (Very Friendly)

This guide walks you through the web demo step by step, even if it’s your first time doing video inpainting.

---

## Where to use the demo

**Online (recommended):**
- Hugging Face: https://huggingface.co/spaces/sczhou/ProPainter  
- OpenXLab: https://openxlab.org.cn/apps/detail/ShangchenZhou/ProPainter

**Local (advanced):**
1. Follow the main README to install dependencies and download weights.
2. Run: `python app.py`
3. Open the URL shown in the terminal (Gradio prints the exact address).

---

## Quick Start (3 steps)

1. **Upload a video** and click **“Get video info.”**
2. **Add masks** (mark what you want to remove).
3. Click **“1. Tracking”**, then **“2. Inpainting.”**

That’s it! The result appears in the right-hand video panel.

---

## Step-by-step (beginner-friendly)

### ✅ Step 1: Upload your video
1. Click the **video upload box** and choose an `.mp4` file.
2. Click **“Get video info.”**
3. You’ll see details like FPS and frame count on the right.

**Tip:** Shorter videos (or lower resolution) run faster.

---

### ✅ Step 2: Add masks (tell ProPainter what to remove)
1. A frame appears in **Step 2**.
2. Use the **“Track start frame”** slider to pick a good frame to mark.
3. Select **Point prompt = Positive**.
4. **Click on the object** you want to remove.  
   - Add a few clicks until the mask covers the object.
5. If the mask spills outside the object:
   - Switch to **Negative** and click the area you want to exclude.
6. Click **“Add mask.”**

**Optional (multiple objects):**
Repeat the steps above, then click **“Add mask”** again.  
Use **Mask selection** to switch between masks.

**If you make a mistake:**
- **Clear clicks** removes only the current clicks.
- **Remove mask** deletes the selected mask.

---

### ✅ Step 3: Track masks and inpaint
1. Click **“1. Tracking.”**  
   This follows your mask through the whole video.
2. Check the **tracking preview** on the left.  
   If it looks wrong, go back to Step 2 and refine the mask.
3. Click **“2. Inpainting.”**  
   The final result appears on the right.

**Download:** Use the video player’s download icon to save the result.

---

## Optional: ProPainter Parameters (safe defaults)
You can open **“ProPainter Parameters”** if you want to adjust speed/quality.

- **Resize ratio**: Lower = faster and less memory (try `0.5` if it’s slow).
- **Mask dilation**: Slightly larger masks can reduce edge artifacts.
- **Sub-video length**: Lower values help very long videos.

If you’re unsure, **leave everything as-is**.

---

## Tips for better results
- Choose a **clear frame** for your first mask.
- Add **3–6 positive clicks** spread across the object.
- Use **negative clicks** to remove areas you don’t want erased.
- If the object changes a lot, try a **different start frame**.

---

## Troubleshooting

**The buttons are hidden or disabled**
- Make sure you clicked **“Get video info.”**

**Tracking or inpainting fails**
- Try a shorter or lower-resolution video.
- Reduce **Resize ratio** (e.g., `0.5`).

**The object is not fully removed**
- Add more positive clicks and re-add the mask.
- Use negative clicks to clean the boundary.

---

## You’re done!
If you want to try it quickly, use the **Examples** section at the bottom of the demo.
