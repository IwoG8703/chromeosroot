# 📱 Root ChromeOS (FydeOS, Brunch Framework) – Complete Guide

Unlock the **full potential** of your ChromeOS-based system by rooting it with the help of **KernelSU**.  
This guide walks you through the process step-by-step — from downloading the patched kernel to installing it into your system.

Whether you're running **FydeOS** or using the **Brunch Framework**, you're in the right place.

> ⚠️ **Disclaimer**  
> Rooting your device may void warranties, break system components, or lead to data loss. Proceed **at your own risk**.

---

## 🚀 What You’ll Need

🛠️ **System Requirements**  
- A Chromium OS setup (FydeOS, Brunch, or similar)  
- Developer Mode **enabled**  
- Terminal access (`Ctrl + Alt + T`)  
- GitHub account (for downloading kernel builds)

📁 **Tools / Files**  
- Prebuilt kernel (`bzImage`) from KernelSU GitHub Actions  
- Basic shell knowledge

---

## 🧩 Rooting Steps

### 🔽 1. Download the Prebuilt Kernel

1. Go to 👉 https://github.com/tiann/KernelSU/actions/workflows/build-kernel-arcvm.yml?query=is%3Asuccess
2. Click the **latest successful** workflow (topmost ✅)
3. Scroll to the bottom and download the artifact:  
   kernel-ARCVM-x86_64-<version>.zip  
   > 📌 *Make sure you're signed into GitHub to access the download link.*

---

### 📦 2. Extract the Patched Kernel

- Open the archive and extract the file:  
  bzImage
- Move `bzImage` to your **Downloads** folder — this is the patched kernel we’ll install.

---

### 🧪 3. Install the Patched Kernel

Open the ChromeOS terminal:

Ctrl + Alt + T

Enter the system shell:

shell

Become root:

sudo bash

Navigate to the Android VM kernel directory:

cd /opt/google/vms/android

(✅ Optional) Backup the original kernel:

mv vmlinux vmlinux.orig

Copy the patched kernel:

cp /home/chronos/user/Downloads/bzImage ./vmlinux

Reboot the system:

sudo reboot

---

## 🎉 Success!

If everything went well — **congrats!** 🥳 Your ChromeOS is now rooted via **KernelSU**.  
You now have enhanced permissions for apps, debugging, and modding.

---

## 📎 References & Resources

- KernelSU GitHub: https://github.com/tiann/KernelSU
- FydeOS Official Site: https://fydeos.io/
- Brunch Framework: https://github.com/sebanc/brunch
- Inspiration – Reddit Tutorial: https://www.reddit.com/r/chromeos/comments/14bwi9r/tutorial_root_your_chromeos_android_subsystem/

---

## 💡 Tips & Notes

- 🔄 You can **restore** the original kernel anytime:
  mv vmlinux.orig vmlinux
  sudo reboot

- 🧯 If something breaks, try booting into recovery or re-flashing your system.
- ⚙️ Consider pairing this root setup with **Magisk**, **ADB**, or **custom system images** for more power.

---

Made with ❤️ by the community.  
PRs, forks, and feedback are welcome!
