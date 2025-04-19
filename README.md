# 📱 Root ChromeOS (FydeOS, Brunch Framework) – Complete Guide

A complete, beginner-friendly guide to rooting ChromeOS-based systems using FydeOS or the Brunch Framework. Whether you're a power user or just getting started, this repository provides clear steps, tools, and tips to help you unlock full root access on your Chromium OS setup.

> ⚠️ **Disclaimer**  
> Rooting your device can void warranties, break system functionality, or render your installation unusable. Proceed with caution and at your own risk.

---

## 🚀 What You’ll Need
- A ChromeOS-based system (FydeOS or Brunch Framework)
- Developer mode enabled
- Access to a Linux shell (`Ctrl + Alt + T`)
- A GitHub account (for downloading build artifacts)

---

## 🛠️ Rooting Steps

### 1. Download the Prebuilt Kernel

- Go to [KernelSU GitHub Actions](https://github.com/tiann/KernelSU/actions/workflows/build-kernel-arcvm.yml?query=is%3Asuccess)
- Click the latest (topmost) workflow with a ✅ tick next to the description
- Scroll to the bottom of the page
- Download the artifact archive:  
  `kernel-ARCVM-x86_64-<version>.zip`  
  > *(Make sure you're logged into GitHub, otherwise the download links may not be clickable)*

---

### 2. Extract the Patched Kernel

- Extract the file `bzImage` from the downloaded archive  
- Move or copy `bzImage` to your **Downloads** folder  
  This is your patched kernel file.

---

### 3. Install the Patched Kernel

Open the ChromeOS terminal:

```sh
Ctrl + Alt + T
```

Then enter the system shell:

```sh
shell
```

Switch to root:

```sh
sudo bash
```

Navigate to the Android subsystem's kernel directory:

```sh
cd /opt/google/vms/android
```

(Optional) Back up the current kernel:

```sh
mv vmlinux vmlinux.orig
```

Copy the new kernel:

```sh
cp /home/chronos/user/Downloads/bzImage ./vmlinux
```

Reboot the system:

```sh
sudo reboot
```

---

## 🎉 Done!

Your ChromeOS-based system is now rooted using the KernelSU-patched kernel!  
Enjoy advanced features and full control over your device.

---

## 📎 References

- [KernelSU GitHub Repository](https://github.com/tiann/KernelSU)
- [FydeOS](https://fydeos.io/)
- [Brunch Framework](https://github.com/sebanc/brunch)

---

## 🧠 Tips

- You can always restore the original kernel by replacing `vmlinux` with `vmlinux.orig`.
- Use this setup only if you're familiar with ChromeOS internals or are willing to experiment.
