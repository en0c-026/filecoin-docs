---
title: "Add to MetaMask"
description: "MetaMask is a popular browser extension that allows users to interact with blockchain applications. This guide shows you how to integrate FIL into MetaMask using the Hyperspace testnet or a local testnet."
lead: "MetaMask is a popular browser extension that allows users to interact with blockchain applications. This guide shows you how to integrate FIL into MetaMask using the Hyperspace testnet or a local testnet. This page assumes that you already have [MetaMask installed](https://metamask.io/) in your browser."
menu:
    developers:
        parent: "developers-how-tos"
        identifier: "add-to-metamask-skljfh12p98y2b7fgto8rwet4"
type: docs
weight: 40
draft: false
images: []
aliases:
    - "/fvm/how-tos/add-to-metamask/"
    - "/developers/smart-contracts/how-tos/add-to-metamask/"
---

You can connect your MetaMask wallet to a Filecoin testnet [automatically by using Chainlist.org](#chainlist). You can also [manually enter](#manual) the testnet variables into MetaMask.

## Chainlist

The easiest way to add a Filecoin testnet to your MetaMask is by using the pre-configured options at chainlist.org.

1. Go to [chainlist.org](https://chainlist.org/).
1. Enable the **Testnets** toggle and enter `Filecoin` into the search bar.

    ![Search for Filecoin testnets in Chainlist.](chainlist-search-for-filecoin-testnets.png)

1. Select the testnet you want to connect to. In this example we are going to connect to the Hyperspace testnet.

1. Scroll down to find the **Filecoin -- Hyperspace** testnet:

    ![Find the Hyperspace testnet.](chainlist-select-hyperspace.png)

1. In MetaMask click **Next**.

    ![Click next in MetaMask.](chainlist-connect-with-metamask.png)

1. Click **Connect**:

    ![Click connect in MetaMask.](chainlist-click-connect-in-metamask.png)

1. Click **Approve** when prompted to _Allow this site to add a network_:

    ![Approve the new network in MetaMask](chainlist-approve-new-network.png)

1. Click **Switch network** when prompted by MetaMask:

    ![Switch networks in MetaMask.](chainlist-switch-network.png)

1. Open MetaMask from the browser extensions tab:

    ![Open MetaMask from the browser extensions tab.](chainlist-open-metamask.png)

1. You should see the Filecoin Hyperspace testnet listed at the top:

    ![MetaMask on the Filecoin Hyperspace testnet.](chainlist-hyperspace-added.png)

## Manual

If you can't or don't want to use Chainlist, you can add a testnet to your MetaMask wallet manually.

{{< tabs tabTotal="2">}}
{{< tab tabName="Hyperspace" >}}
<br>

1. Open your browser and open the MetaMask plugin.
2. Click the user circle at the top right and select **Settings**:
3. Select **Networks**.
4. Click **Add a network**.
5. Scroll down and click **Add a network manually**.
6. Enter the following information into the fields:

    | Field | Value |
    | --- | --- |
    | Network name | `Filecoin Hyperspace testnet` |
    | New RPC URL | `https://api.hyperspace.node.glif.io/rpc/v1` |
    | Chain ID | `3141` |
    | Currency symbol | `tFIL` |

7. Pick one of the following block explorers, and enter the URL into the **Block explorer (optional)** field:

    - Glif Explorer: `https://explorer.glif.io/?network=hyperspace`
    - Filscan: `https://hyperspace.filscan.io/`

8. Review the values in the fields and click **Save**.
9.  The Hyperspace testnet should now be shown in your MetaMask window.
10. Done!


{{< /tab >}}
{{< tab tabName="Local-testnet" >}}
<br>

1. Ensure you have set `EnableEthRPC` to `true` within your Lotus client's `config.toml file.
1. Open your browser and open the MetaMask plugin.
2. Click the user circle at the top right and select **Settings**:
3. Select **Networks**.
4. Click **Add a network**.
5. Scroll down and click **Add a network manually**.
6. Enter the following information into the fields:

    | Field | Value |
    | --- | --- |
    | Network name | `Filecoin local testnet` |
    | New RPC URL | `http://localhost:1234/rpc/v1` |
    | Chain ID | `31415926` |
    | Currency symbol | `tFIL` |

7. Pick one of the following block explorers, and enter the URL into the **Block explorer (optional)** field:

    - Glif Explorer: `https://explorer.glif.io/?network=hyperspace`
    - Filscan: `https://hyperspace.filscan.io/`

8. Review the values in the fields and click **Save**.
9. Your MetaMask wallet should now be connected to your local testnet!

{{< /tab >}}
{{< /tabs >}}

## Next steps

You can now add funds to your [MetaMask wallet]({{< relref "get-test-funds" >}}) and [deploy a contract]({{< relref "deploy-a-contract" >}})!
