# Verbene

**See what your Mac is doing, and whether it's behaving normally.**

Verbene shows your Mac's activity live (CPU, GPU, memory, disk, network, energy and temperatures), down to each process. It also runs controlled stress tests of the hardware, with safety limits, so you can see how your Mac holds up under sustained load.

Download Verbene from [Releases](../../releases). Report bugs and suggest features in [Issues](../../issues/new/choose).

## Requirements

- A Mac with **Apple Silicon** (M1 or later). Intel Macs are not supported.
- **macOS Sequoia 15** or newer. Supported: Sequoia 15, Tahoe 26 and Golden Gate 27.

## Install

Verbene is currently in **beta**. Beta builds are marked *Pre-release*.

1. Download the newest `Verbene-<version>.dmg` from [Releases](../../releases).
2. Optional but recommended: check that the download is intact. In Terminal, run the command below and compare the result with the SHA-256 in the release notes.
   ```bash
   shasum -a 256 ~/Downloads/Verbene-*.dmg
   ```
3. Open the DMG and drag **Verbene** onto **Applications**. Always run Verbene from Applications, not from the DMG.
4. Open Verbene. macOS says it cannot verify the developer. Click **Done** (not Move to Trash).
5. Open **System Settings → Privacy & Security**, scroll down, click **Open Anyway** next to the Verbene message, and authenticate. Verbene now opens.

During the beta, builds are signed but not yet notarized by Apple, which is why step 5 is needed. It approves only Verbene; Gatekeeper stays on for everything else.

### Optional: full process coverage

Without extra permission, macOS doesn't let Verbene read processes that belong to macOS or to other users; Verbene shows those as not readable. To include them:

1. Open **Verbene → Settings…** (⌘,) and click **Turn On…** under *Full process coverage*.
2. In the System Settings window that opens (**General → Login Items & Extensions**), switch **Verbene** on under *Allow in the Background*.
3. Back in Verbene, the status shows **On**.

This installs a small helper that runs as an administrator and only reads process activity. You can turn it off at any time in the same place.

## Update

Quit Verbene, drag the new version over the old one in Applications, and do the **Open Anyway** step again (it is needed for every new build). If *Full process coverage* then shows *Waiting for approval*, switch Verbene on again in Login Items & Extensions.

## Uninstall

1. In **Verbene → Settings…**, click **Turn Off** under *Full process coverage* (if you turned it on).
2. Quit Verbene and move it from Applications to the Trash.

Deleting the app before turning the helper off leaves a stale entry in Login Items & Extensions, which you can remove there.

## Report a bug or request a feature

Open an [issue](../../issues/new/choose) and choose **Bug report** or **Feature request**. You need a free GitHub account. For bugs, please include your macOS version, Mac model and Verbene build (**Verbene → About Verbene**). Screenshots help, but crop out anything private.

## Acknowledgments

Verbene is developed with the assistance of [Claude](https://www.anthropic.com/claude), Anthropic's AI model.
