### ⚡️ Follow these instructions to access Langflow on Github Codespaces
To make life easier, we'll use the awesome Github Codespace functionality. Github offers you a smooth cloud-based developer experience to get started quickly. How?

1. Open the [watsonx-langflow-agent](https://github.com/jpradier/WatsonX-Langflow) repository
2. Click on `Use this template`->`Open in a codespace` as follows:

    ![github-open-in-codespace](./assets/github-open-in-codespace.png)

    🎉 Congratulations, you just started your cloud IDE in which we'll work from here.

    💡 In case you want to keep you changes, you can also opt to 'fork' the repo by clicking `Create a new repository`. This will also enable you to check out the code locally and run from your own machine.  

5. Configure the secrets as follows:

- Copy `.env.example` and then paste it. Now rename the copy to `.env`

    ![codespace](./assets/codespaces.png)

- Edit `.env` and provide the required variables:
    - `WATSONX_PROJECT_ID` (your watsonx.ai project ID)
    - `WATSONX_API_ENDPOINT` (your watsonx.ai endpoint, e.g. `https://us-south.ml.cloud.ibm.com`)
    - `WATSONX_API_KEY` (your watsonx.ai API key)
    - `ASTRA_DB_API_ENDPOINT` and `ASTRA_DB_APPLICATION_TOKEN`

6. Now we can run Langflow as follows in the terminal window:

    ```bash
    pip install uv
    uv sync
    uv run langflow run --env-file .env
    ```
    ![run-langflow](./assets/run-langflow.png)

    This starts Langflow and opens a port to your Codespace in the cloud. Click `Make Public` to ensure you can access Langflow from anywhere on the internet.

    ![codespace-forward-port](./assets/codespace-forward-port.png)

    Now navigate to `PORTS` which shows you all forwarded ports from the Codespace, click on the `Forwarded Address` for Langflow and click the globe icon to open Langflow in a browser

    ![codespace-ports](./assets/codespace-ports.png)

    💡 In case you lose track of the URL to Langflow, just click on `PORTS` again in the terminal window.

    ⚠️ Ensure the Port Visibility is set to Public, especially important for the MCP server part later on in this tutorial!

    ![codespace-public-port](./assets/codespace-public-port.png)

🎉 Congrats! You finished the set-up part of the workshop. Now for the fun part!
----

<-- Go back to the [Langflow Lab instructions](./README.md)