# Time Synchronization Protocols in Casio Multiband 6

Below is a list of radio protocols (time signals) used by stations supported by **Casio Multiband 6**, along with detailed information about each one.

## Supported Protocols

1. **JJY (Japan)** — 40 kHz (Fukushima) and 60 kHz (Kyushu)
2. **WWVB (USA)** — 60 kHz (Fort Collins, Colorado)
3. **MSF (United Kingdom)** — 60 kHz (Anthorn)
4. **DCF77 (Germany)** — 77.5 kHz (Mainflingen)
5. **BPC (China)** — 68.5 kHz (Shanxi)

## Protocol Details

### JJY (Japan)
- **Frequencies:** 40 kHz (JJY40, Fukushima) and 60 kHz (JJY60, Kyushu).
- **Modulation:** amplitude (on/off keying).
- **Frame structure:** 60-second frame where each second pulse encodes one data bit.
- **Bit encoding:** duration of carrier drop within the second (typically 0.2 s for “0” and 0.5 s for “1”).
- **Data transmitted:** precise time, date, year number, day of week, leap second information, and daylight saving time transitions.
- **Notes:** two transmitters improve reception reliability across Japan.

### WWVB (USA)
- **Frequency:** 60 kHz (Fort Collins, Colorado).
- **Modulation:** amplitude; phase modulation is also used in newer implementations for improved robustness.
- **Frame structure:** 60-second frame with 60 bits.
- **Bit encoding:** duration of carrier amplitude reduction within the second (0.2 s, 0.5 s, 0.8 s).
- **Data transmitted:** UTC time, date, daylight saving time indicators, and high-accuracy flags.
- **Notes:** widely used standard for radio time synchronization in North America.

### MSF (United Kingdom)
- **Frequency:** 60 kHz (Anthorn).
- **Modulation:** amplitude (on/off keying).
- **Frame structure:** 60-second frame with minute structure.
- **Bit encoding:** duration of carrier drop within the second (typically 0.1 s for “0”, 0.2 s for “1”, 0.5 s for markers).
- **Data transmitted:** UTC time, date, daylight saving time indicators, leap second information.
- **Notes:** primary radio time signal for the United Kingdom.

### DCF77 (Germany)
- **Frequency:** 77.5 kHz (Mainflingen, near Frankfurt).
- **Modulation:** amplitude; phase modulation on modern receivers.
- **Frame structure:** 59 data bits per minute, 60th second is the frame marker.
- **Bit encoding:** amplitude reduction for 0.1 s (“0”) or 0.2 s (“1”) at the start of the second.
- **Data transmitted:** UTC/CET/CEST time, date, transition flags, leap seconds.
- **Notes:** one of the most widely used European time signals.

### BPC (China)
- **Frequency:** 68.5 kHz (Shanxi).
- **Modulation:** amplitude.
- **Frame structure:** minute-long frame with bitwise data transmission.
- **Bit encoding:** carrier drop duration, similar to other longwave time stations.
- **Data transmitted:** UTC time, date, transition information, leap seconds.
- **Notes:** provides synchronization within China and neighboring regions.

---

If you want to add more stations or expand a specific protocol description, let me know and I will help extend it.
