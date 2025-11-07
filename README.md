<p align="center">
  <img src="council.png" alt="World council of ten shadowed members at a glowing table deciding the fate of the world" width="400">
</p>


# The Council

Ask the council for deliberation.

This is a local Flask web app that lets you ask a group of distinct AI personas for advice.  
Each persona proposes one option, then all personas score every option from 0 to 100.  
The app averages the scores and highlights the council choice.

---

## Caveats and limitations

This is a local prototype, not a production system.

* The API key is kept in `app.py` by default. That is convenient but not safe for shared deployments
* There is no authentication, rate limiting, logging or monitoring
* There is no persistent reputation system yet, so members do not learn across sessions


Use this as a local tool and as a base for experiments.

---

## Quick start

### Requirements

* Python 3.9 or newer
* An OpenAI compatible API key with access to `gpt-4.1-mini` or any other chat model you choose

### Install and run

Clone the repository and set up a virtual environment:

```bash
git clone https://github.com/Luvvydev/The-Council.git
cd The-Council

python3 -m venv .venv
source .venv/bin/activate

python3 -m pip install --upgrade pip
python3 -m pip install flask openai
