📱 Root ChromeOS (FydeOS / Brunch Framework)

> 🇵🇱 Kliknij, żeby rozwinąć wersję polską  
> 🇬🇧 Click to expand English version

======================
🇬🇧 English – Complete Guide
======================

📱 Root ChromeOS (FydeOS, Brunch Framework) – Complete Guide

Unlock the full potential of your ChromeOS-based system by rooting it with the help of KernelSU.
This guide walks you through the process step-by-step — from downloading the patched kernel to installing it into your system.

Whether you're running FydeOS or using the Brunch Framework, you're in the right place.

⚠️ Disclaimer
Rooting your device may void warranties, break system components, or lead to data loss. Proceed at your own risk.

🚀 What You’ll Need

System Requirements:
- A Chromium OS setup (FydeOS, Brunch, or similar)
- Developer Mode enabled
- Terminal access (Ctrl + Alt + T)
- GitHub account (for downloading kernel builds)

Tools / Files:
- Prebuilt kernel (bzImage) from KernelSU GitHub Actions
- Basic shell knowledge

🧩 Rooting Steps

1. Download the Prebuilt Kernel
   - Go to: https://github.com/tiann/KernelSU/actions/workflows/build-kernel-arcvm.yml?query=is%3Asuccess
   - Click the latest successful workflow
   - Download kernel-ARCVM-x86_64-<version>.zip

2. Extract the Patched Kernel
   - Extract bzImage from the ZIP file
   - Move to Downloads

3. Install the Patched Kernel
   - Open terminal (Ctrl + Alt + T)
   - Commands:
     shell
     sudo bash
     cd /opt/google/vms/android
     mount -o remount,rw /
     mv vmlinux vmlinux.orig
     cp /home/chronos/user/Downloads/bzImage ./vmlinux
     sudo reboot

🎉 Success!
You're now rooted via KernelSU.

📎 Resources:
- KernelSU: https://github.com/tiann/KernelSU
- FydeOS: https://fydeos.io/
- Brunch: https://github.com/sebanc/brunch
- Reddit Guide: https://www.reddit.com/r/chromeos/comments/14bwi9r/tutorial_root_your_chromeos_android_subsystem/

Tips:
- Restore:
  mv vmlinux.orig vmlinux
  sudo reboot

======================
🇵🇱 Wersja Polska – Kompletny Poradnik
======================

📱 Root ChromeOS (FydeOS, Brunch Framework) – Kompletny Poradnik

Odblokuj pełny potencjał swojego systemu ChromeOS dzięki rootowi przez KernelSU.
Ten poradnik przeprowadzi Cię krok po kroku — od pobrania kernela po jego instalację.

Jeśli używasz FydeOS albo Brunch Framework – jesteś we właściwym miejscu.

⚠️ Uwaga
Rootowanie może unieważnić gwarancję, uszkodzić system lub doprowadzić do utraty danych. Robisz to na własne ryzyko.

🚀 Co będzie potrzebne

Wymagania systemowe:
- System oparty na Chromium OS (FydeOS, Brunch itd.)
- Włączony Tryb Dewelopera
- Dostęp do terminala (Ctrl + Alt + T)
- Konto GitHub (do pobrania kernela)

Pliki i narzędzia:
- Gotowy kernel (bzImage) z GitHub Actions projektu KernelSU
- Podstawowa znajomość terminala

🧩 Kroki rootowania

1. Pobierz gotowy kernel
   - Wejdź na: https://github.com/tiann/KernelSU/actions/workflows/build-kernel-arcvm.yml?query=is%3Asuccess
   - Kliknij w najświeższy sukces
   - Pobierz kernel-ARCVM-x86_64-<wersja>.zip

2. Wypakuj kernel
   - Rozpakuj ZIP i wyciągnij plik bzImage
   - Przenieś do folderu Downloads

3. Zainstaluj nowy kernel
   - Otwórz terminal (Ctrl + Alt + T)
   - Komendy:
     shell
     sudo bash
     cd /opt/google/vms/android
     mount -o remount,rw /
     mv vmlinux vmlinux.orig
     cp /home/chronos/user/Downloads/bzImage ./vmlinux
     sudo reboot

🎉 Sukces!
Masz teraz roota przez KernelSU.

📎 Linki i źródła:
- KernelSU: https://github.com/tiann/KernelSU
- FydeOS: https://fydeos.io/
- Brunch: https://github.com/sebanc/brunch
- Reddit: https://www.reddit.com/r/chromeos/comments/14bwi9r/tutorial_root_your_chromeos_android_subsystem/

Porady:
- Przywracanie:
  mv vmlinux.orig vmlinux
  sudo reboot
