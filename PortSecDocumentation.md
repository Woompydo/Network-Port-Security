This documentation will guide you through configuring port security. Port security restricts which devices can connect to a physical switch port using a cable by checking their MAC addresses.

## Step 1: Setting Up the Devices

We'll add some basic devices, including two laptops and a switch. Each laptop will demonstrate a different type of security violation. What's that, you may ask? Well, there are three types of security violations that I'll explain to you.

Protect: Blocks traffic from unauthorized devices but keeps the switch port active.
Restrict: Blocks unauthorized traffic and records the violation, usually by increasing a counter and sending a log message.
Shutdown: Disables the switch port when a security violation occurs. The port must be reactivated before it can work again.

Protect and Restrict are quite similar. Both block traffic from unauthorized devices, but Restrict also records the violation. In other words, Restrict offers an additional feature compared to Protect. So, we'll focus on testing the Shutdown and Restrict violation modes.
