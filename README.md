# AudioShare

Welcome to the AudioShare repository, a streamlined solution for sharing computer audio over a microphone. This versatile tool works across all Linux distributions, enabling users to transmit any computer audio during calls on platforms like Discord, Telegram, and more. The following instructions predominantly use Fedora (for users with pure PipeWire) and Manjaro (for those using pipewire-pulse).

## Important Note
While this guide is based on Fedora and Manjaro for ease of explanation, **the principles should apply to any Linux distribution**. Furthermore, it is important to highlight that over the years it is natural for most distributions to start migrating to pure PipeWire, as it is a more modern solution than PulseAudio.

## Features

- Simple and direct system audio sharing.
- Creation of a virtual microphone, usable across various conferencing applications.
- Individual volume control for audio sharing.
- High compatibility with different Linux distributions.
  

## Getting Started

### Requirements

- [PipeWire](https://pipewire.org/) or [pipewire-pulse](https://archlinux.org/packages/extra/x86_64/pipewire-pulse/)
- [Helvum](https://flathub.org/apps/org.pipewire.Helvum)
- Basic knowledge of command-line interface

### Installation

1. Clone the repository

    ```bash
    git clone https://github.com/yesmanic/AudioShare.git
    ```

2. Navigate to the project directory

    ```bash
    cd AudioShare
    ```
###  Check your Server Stream

To begin, determine whether your system uses PipeWire or PulseAudio in compatibility mode with pipewire-pulse. You can use the following commands to check your audio manager. The command that does not return an error, such as "unknown module," indicates your current server stream of audio manager.

For PulseAudio:
```bash
systemctl --user status pulseaudio
```

For PipeWire:
```bash
systemctl --user status pipewire
```

### Environment Setup

Once you have identified your server, proceed according to the corresponding instructions provided below:

<details>
    <summary markdown="span"><strong>PipeWire</strong></summary>
    

</details>

<details>
    <summary markdown="span"><strong>PulseAudio</strong></summary>
    <!-- detailed PulseAudio setup instructions go here -->
</details>

### Configuring Audio Toggle

For setting up an audio toggle to easily switch between standard audio and shared microphone audio.

## Final Result

After setting up your `.sh` scripts successfully, they can be used as you feel comfortable. We recommend configuring them to start with the system. If execution is incomplete, likely due to `sleep` commands in the **bash scripts**, you may need to adjust the sleep durations based on your computer's boot speed.

Once the scripts are executed, open Helvum. The application should appear as described in this image:

<img src="images/finalHelvum.png" width="100%"  alt="Illustrative picture">

If everything is OK, **Congratulations**, you have configured audio sharing on your system!

## Conclusion

The flexibility Linux offers has turned what once seemed like a limiting factor into a functional and straightforward feature. AudioShare exemplifies how we can leverage Linux's capabilities to enhance our digital interaction experiences.
