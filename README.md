# Friendship Traffic Police 🚦👮‍♀️

A funny one-tap page that tells you how angry she is with you, without her having to talk to you. She plays the traffic cop, you're the doodle stuck in a little pink car, and her verdict comes to your phone.

1. **Caught!** A night road with siren lights flashing. You're sweating in your car going "officer pls 🥺". She taps **Take charge**.
2. **The verdict.** She taps one of 5 traffic lights. Each light plays its own animation:
   - 🟢 **Fine, go:** you honk and zoom away
   - 🟡 **Slow down, still annoyed:** you crawl at 2 km/h and an uncle on a cycle overtakes you
   - 🟠 **Pull over, you're in trouble:** siren, and a ₹5000 fine slaps onto your windshield
   - 🔴 **License cancelled. Don't talk to me:** a tow truck drags your car away while you run after it crying
   - 🚫 **Road closed for a week:** a barricade drops and you wait out "day 1 of 7… day 7 of 7 🍱"

   She can **change her verdict** as many times as she likes. You get notified every time, so you'll know if she softens.
3. **The fine.** She picks any of momos, pizza, biryani, waffle, bhaji, pasta, juice, "do my work for a day" or "a proper sorry in person", or writes her own. She can also skip the fine ("just stay away") and yell something at you in an optional box.
4. **The challan.** A traffic ticket prints out with her verdict and fine, and a "VERDICT RECEIVED. OFFENDER WILL BEHAVE 🫡" stamp drops on it. Then your ending line appears, which depends on the verdict. She can **save the challan** as an image or **tear it up**.

There are no runaway buttons and no forced "yes". Every answer is allowed.

## 1. Personalize it

Open `index.html` and edit the `CONFIG` block at the top of the `<script>`:

- `name`, `fromName`: her name and yours
- `crime`: the line printed under "Crime" on the challan
- `lights`: the 5 verdicts. For each one, `label` is what she taps, `react` is what you say when she hovers it, and `ending` is your line at the very end.
- `fines`: the fine options she can pick
- `sound`: whether sounds start on (she can always mute them with 🔊)

## 2. Get her verdict on your phone

1. Install the **ntfy** app ([Android](https://play.google.com/store/apps/details?id=io.heckel.ntfy) / [iPhone](https://apps.apple.com/app/ntfy/id1625396347)).
2. Subscribe to the topic in `CONFIG.ntfyTopic` (`traffic-cop-c7dc4567e670` right now), or watch it at https://ntfy.sh/traffic-cop-c7dc4567e670
3. You'll get alerts like:
   - `👀 Jasmine opened the traffic police page (phone)`
   - `🚦 Verdict: 🟠 PULL OVER, YOU'RE IN TROUBLE`
   - `🔁 Changed verdict from 🔴 License cancelled… → 🟡 Slow down, still annoyed`
   - `🧾 Jasmine printed the challan`, followed by the verdict, the fine and anything she yelled
   - `👋 Jasmine switched away before giving a verdict`
   - `📸 Jasmine saved the challan` / `🗑️ Jasmine tore up the challan`

Anyone who knows the topic name can read it, so keep it private. Set `ntfyTopic: ""` to turn alerts off, and `showTrackingNote: false` to hide the "this page tells … your verdict" line.

To play through it yourself before sending, temporarily set `ntfyTopic: ""` so you don't get pinged, then put the topic back. Use **start over** at the end to replay.

## 3. Share it

It's a single `index.html` with nothing else needed. Host the `anger meter` folder (or the whole `3dpage` folder) for free and send her the link. The easiest way is to drag the folder onto https://app.netlify.com/drop. GitHub Pages or Vercel also work.
