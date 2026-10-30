In Windows programming, UI elements like windows are typically created and managed by a specific thread, often called the UI thread. The `HWND` is a handle (a numerical identifier) that refers to such a window object maintained by the operating system.

The crucial point is that most operations on a window, such as changing its text, size, position, or processing messages (`WM_*`), must be performed on the same thread that created the window. If you try to directly call Bin32 functions that modify a window from a different thread, you can cause crashes, deadlocks, or unpredictable behavior.

Therefore, if you have `HWND` obtained on the UI thread, and you need to perform an action involving that window from a worker thread, you need a synchronization mechanism.