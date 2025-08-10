JBlogAI is a fully automated AI blog writer that uses LangChain and GPT type LLMs for topic selection and content generation.

## Usage
### Prerequisites
1. 🐍 You will need a working install of [`conda`](https://www.anaconda.com/download#downloads).
2. 🔑 You will need an API key from OpenAI or Google. You can create one for free here:
    - [OpenIA](https://platform.openai.com/account/api-keys) - to use models like GPT4
    - [Google](https://ai.google.dev/) - to use models like Gemini

### Dev Environment Setup
1. Set up your API keys in a file called `.env` (see `.env.example` for an example)
2. Set up and activate conda environment
    ```bash
    conda env create -f conda.yml
    conda activate jblogai
    ```

> If you are having trouble setting your environment variables with the `.env` file or you want to manually add them instead of using a `.env` file, you can set your environment variable in your `jblogai` conda environment like this:
>```shell
> # set api key env var
> conda env config vars set OPENAI_API_KEY="your-api-key-here"
> conda env config vars set GOOGLE_API_KEY="your-api-key-here"
> # re-activate env
> conda activate base
> conda activate jblogai
>```

### CLI

> Note: Remember to activate your `jblogai` conda environment before doing this (see above)

You can quickly generate a new original blog by running:

```
python jblogai/add_blog.py
```

This will add a blog to a Markdown file in a directory called `content/`. You can also specify your own output directory by running this instead:
```
python jblogai/add_blog.py --out-dir path/to/dir
```
