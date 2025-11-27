
# 0xio Ecosystem Directory

Welcome to the official repository for the **0xio Ecosystem Directory**.

This repository serves as the source of truth for all projects, dApps, and tools listed on [0xio.xyz/ecosystem](https://0xio.xyz/ecosystem). We believe in open-source collaboration, if you are building on the Octra Network, we want you listed.

## How to Submit Your Project

Adding your project is as simple as creating a JSON file and submitting a Pull Request.

### 1. Fork & Clone

Fork this repository to your own GitHub account and clone it locally.

```bash
git clone https://github.com/0xio-xyz/ecosystem.git
cd ecosystem
````

### 2\. Edit the Projects File

Open the `projects.json` file in your text editor. This file contains an array of all ecosystem projects.

### 3\. Append Your Project
#### ⚠️ IMPORTANT: DO NOT delete or modify existing projects. Just append your new project object to the end of the array.

1. Scroll to the bottom of the JSON array.

2. Check the `id` of the last project in the list.

3. Add a new object for your project, incrementing the `id` by 1.

Example:

```json
 ...
    {
      "id": 9,
      "name": "Existing Project",
      ...
    }, 
    {
      "id": 10,
      "name": "My Octra dApp",
      "description": "A brief, high-impact description of what your project does and how it uses FHE on Octra.",
      "categories": [
        "DeFi",
        "Privacy"
      ],
      "status": "Testnet",
      "logoUrl": "[https://gateway.pinata.cloud/ipfs/QmYourImageHash](https://gateway.pinata.cloud/ipfs/QmYourImageHash)...",
      "link": "[https://my-octra-dapp.xyz](https://my-octra-dapp.xyz)",
      "twitter": "[https://twitter.com/myoctradapp](https://twitter.com/myoctradapp)"
    }
  ]
```

### 4\. Submit Pull Request

Commit your changes and push them to your fork. Then, open a Pull Request (PR) against the ```main``` branch of this repository.

PR Title: ```feat: add <Project Name>```

Description: Briefly explain what your project is.

## Schema Documentation

| Field | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `id` | `string` | **Yes** | Incremental Integer. Check the last project ID in the list and increment by 1. |
| `name` | `string` | **Yes** | The display name of your project. |
| `description` | `string` | **Yes** | Max 200 characters. Keep it punchy. |
| `categories` | `array` | **Yes** | Choose from the Allowed Categories list below. |
| `status` | `string` | **Yes** | `Live`, `Testnet`, or `Dev`. |
| `logoUrl` | `string` | **Yes** | Direct URL to a square PNG/SVG logo (min 256x256). **We recommend using [Pinata](https://pinata.cloud) (IPFS) for storage.** |
| `link` | `string` | Yes | The main URL for your dApp or website. |
| `twitter` | `string` | Yes | Full URL to your X/Twitter profile. Set to "" or omit if not applicable. |

### Allowed Categories

Please select **1-3** categories that best describe your project:

  * `Wallet`
  * `DeFi`
  * `Infrastructure`
  * `Privacy`
  * `Tooling`
  * `Game`
  * `Education`

## Review Process

1.  **Automated Checks:** Our CI will verify that your JSON is valid and adheres to the schema.
2.  **Manual Review:** The 0xio team will review the content to ensure it meets our quality standards and verify the project is legitimately building on Octra.
3.  **Merge:** Once approved, your project will automatically appear on the ecosystem page within a few minutes.

## ❓ Need Help?

If you have questions or need assistance, please [open an issue](https://github.com/0xio-xyz/ecosystem/issues).
