This documentation will guide you through configuring port security. Port security restricts which devices can connect to a physical switch port using a cable by checking their MAC addresses.

## Step 1: Setting Up the Devices

We'll add some basic devices, including two laptops and a switch. Each laptop will demonstrate a different type of security violation. What's that, you may ask? Well, there are three types of security violations that I'll explain to you.

- **Protect**: Blocks traffic from unauthorized devices but keeps the switch port active.
- **Restrict**: Blocks unauthorized traffic and records the violation, usually by increasing a counter and sending a log message.
- **Shutdown**: Disables the switch port when a security violation occurs. The port must be reactivated before it can work again.

Protect and Restrict are quite similar. Both block traffic from unauthorized devices, but Restrict also records the violation. In other words, Restrict offers an additional feature compared to Protect. So, we'll focus on testing the Shutdown and Restrict violation modes.

<img width="410" height="236" alt="image" src="https://github.com/user-attachments/assets/c01e1bdd-3087-4d65-9f8f-610ae4b5f940" />

In the image above, we have a switch, two PCs, and another PC that will attempt to attack the switch port.


## Step 2: Configuring the PC & Switch

Make sure to configure the PCs first by assigning them IP addresses. Then, verify that you can send PDUs between the PCs connected to the switch.

Why do we do this? Because we want the switch to learn the MAC addresses of the connected devices. We'll be using Sticky to automatically add the learned MAC addresses to the switch's port security configuration. However, there are two ways to do this:

**Sticky**: This allows the switch to learn MAC addresses automatically and add them to the port security configuration. We'll use this method because it's simpler.

**Manual**: This requires us to manually enter the MAC addresses into the switch's port security configuration.





