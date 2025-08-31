
# 📱 Root ChromeOS (Stock / FydeOS / Brunch Framework) – Like a Boss

> 🇵🇱 Kliknij, żeby rozwinąć wersję polską  
> 🇬🇧 Click to expand English version

<details>
<summary>🇬🇧 English – Complete Guide</summary>

## 📱 Root ChromeOS – The Fun Way 😎

Ever looked at your Chromebook and thought, “I can totally make you more awesome”?  
Well, now you can — with the magic of **KernelSU** and a little sprinkle of **terminal wizardry**.

> ⚠️ **Disclaimer**  
> Rooting your system may cause spontaneous combustion of boredom. Also: void warranties, break stuff, or delete your memes. You’ve been warned.

---

## 🚀 What You’ll Need

🛠️ **Checklist:**  
- A Chromium OS beast (FydeOS, Brunch, Stock ChromeOS (NOT FLEX!) – not your grandma’s OS)  
- Developer Mode: ON (no excuses)  
- Terminal skills: minimal, but bold  
- GitHub account: because downloading random kernels from strangers is a hobby now

📁 **Tools**  
- Prebuilt kernel (aka `bzImage`, your new best friend)  
- Your bravery

---

## 🧩 Steps to Greatness

### 🔽 1. Download the Prebuilt Kernel

1. Head over to 👉 https://github.com/tiann/KernelSU/actions/workflows/build-kernel-arcvm.yml?query=is%3Asuccess  
2. Click the **latest green checkmark of destiny**  
3. Scroll down and grab:  
   `kernel-ARCVM-x86_64-<version>.zip`  
   > 📌 Login required. GitHub wants to know you're serious.

---

### 📦 2. Extract the Kernel Goodness

- Unzip the file  
- Fish out the `bzImage`  
- Toss it into your `Downloads` folder like a pro

---

### 🧪 3. Install It Like a Hacker

```sh
Ctrl + Alt + T        # open terminal
```

```sh
shell                # become one with the system
```

```sh
sudo bash            # go full root mode
```

```sh
cd /opt/google/vms/android
mount -o remount,rw /
mv vmlinux vmlinux.orig      # optional: in case stuff goes sideways
cp /home/chronos/user/Downloads/bzImage ./vmlinux
sudo reboot
```

---

## 🎉 You Did It!

If your laptop didn't explode and you still see this — congrats, you're rooted.  
Now go forth and mod everything.

---

## 📎 Useful Links

- KernelSU: https://github.com/tiann/KernelSU  
- FydeOS: https://fydeos.io/  
- Brunch: https://github.com/sebanc/brunch  
- Reddit Guide: (aka the nerd scrolls):  
  https://www.reddit.com/r/chromeos/comments/14bwi9r/tutorial_root_your_chromeos_android_subsystem/

---

## 💡 Extra Nerd Tips

```sh
# Undo the magic (just in case)
mv vmlinux.orig vmlinux
sudo reboot
```

- If it breaks, reflash and pretend it was all a dream  
- Pair it with Magisk or ADB for maximum mayhem

</details>

<details>
<summary>🇵🇱 Wersja Polska – Kompletna Instrukcja</summary>

## 📱 Root ChromeOS – Wersja „Na Grubo” 😜

Patrzysz na swojego Chromebooka i myślisz: „Da się lepiej”?  
No to da się — z **KernelSU** i odrobiną magii terminala ✨

> ⚠️ **Uwaga**  
> Rootowanie może spowodować nagły przypływ mocy, unieważnić gwarancję i wysłać twoje dane w zaświaty. Robisz to na własne ryzyko (i satysfakcję).

---

## 🚀 Co będzie potrzebne

🛠️ **Lista gadżetów:**  
- ChromeOS-owy potworek (FydeOS, Brunch, Stock ChromeOS (NIE FLEX!) - nie coś egzotycznego)  
- Tryb dewelopera: oczywiście że włączony  
- Terminal: minimum wiedzy, maksimum odwagi  
- Konto GitHub: bo ściąganie kerneli to już styl życia

📁 **Pliki i magia**  
- Gotowy kernel (`bzImage`, aka Król Systemu)  
- Odwaga + 1 kubek herbaty

---

## 🧩 Krok po kroku do chwały

### 🔽 1. Pobierz kernel (czyli bazę mocy)

1. Klikaj śmiało 👉 https://github.com/tiann/KernelSU/actions/workflows/build-kernel-arcvm.yml?query=is%3Asuccess  
2. Wybierz najnowszy zielony ✅ (ten z aurą sukcesu)  
3. Na dole weź:  
   `kernel-ARCVM-x86_64-<wersja>.zip`  
   > 📌 Musisz być zalogowany – GitHub nie ufa anonimowym rootującym ninja

---

### 📦 2. Wypakuj jądro (to systemowe)

- Rozpakuj ZIPa  
- Weź `bzImage`  
- Wrzuć do folderu `Downloads` – jak rasowy rootmaster

---

### 🧪 3. Czas na czary w terminalu

```sh
Ctrl + Alt + T        # otwierasz wrota systemu
```

```sh
shell                # tryb wtajemniczenia
```

```sh
sudo bash            # pełna moc administratora
```

```sh
cd /opt/google/vms/android
mount -o remount,rw /
mv vmlinux vmlinux.orig      # (opcjonalna kopia bezpieczeństwa)
cp /home/chronos/user/Downloads/bzImage ./vmlinux
sudo reboot
```

---

## 🎉 Sukces!

Jeśli ekran nie eksplodował — gratulacje, jesteś zrootowany.  
Możesz teraz modować, hakować i rządzić.

---

## 📎 Linki dla wtajemniczonych

- KernelSU: https://github.com/tiann/KernelSU  
- FydeOS: https://fydeos.io/  
- Brunch: https://github.com/sebanc/brunch  
- Redditowa Bibla Rootowania:  
  https://www.reddit.com/r/chromeos/comments/14bwi9r/tutorial_root_your_chromeos_android_subsystem/

---

## 💡 ProTipy

```sh
# Cofnij czary
mv vmlinux.orig vmlinux
sudo reboot
```

- Jak coś się wykrzaczy — flashuj i udawaj, że tak miało być  
- Magisk, ADB i inne bajery – dodaj do zestawu dla pełnej władzy

</details>
