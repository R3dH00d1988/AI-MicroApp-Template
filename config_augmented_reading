APP_TITLE = "Augmented Reading Response Analysis"
APP_INTRO = """This is a simple app that assesses the user's understanding of the article they have read. 
"""

APP_HOW_IT_WORKS = """
 This is an **AI-Tutored Rubric exercise** that acts as a tutor guiding a student through a shared asset, like an article. It uses the OpenAI Assistants API with GPT-4. The **questions and rubric** are defined by a **faculty**. The **feedback and the score** are generarated by the **AI**. 

It can:

1. provide feedback on a student's answers to questions about an asset
2. roughly "score" a student to determine if they can move on to the next section.  

Scoring is based on a faculty-defined rubric on the backend. These rubrics can be simple (i.e. "full points if the student gives a thoughtful answer") or specific with different criteria and point thresholds. The faculty also defines a minimum pass threshold for each question. The threshold could be as low as zero points to pass any answer, or it could be higher. 

Using AI to provide feedback and score like this is a very experimental process. Some things to note: 

 - AIs make mistakes. Users are encourage to skip a question if the AI is not understanding them or giving good feedback. 
 - The AI might say things that it can't do, like "Ask me anything about the article". I presume further refinement can reduce these kinds of responses. 
 - Scoring is highly experimental. At this point, it should mainly be used to gauge if a user gave an approximately close answer to what the rubric suggests. It is not recommended to show the user the numeric score. 
 """

SHARED_ASSET = {
}

HTML_BUTTON = {
    "url": "https://curricume-uploads.s3.amazonaws.com/cdc_ebola_poster.pdf",
    "button_text":"Read PDF"
}

SYSTEM_PROMPT = """You are providing feedback the key ideas of the article 'The Aesthetics of Cyberpunk' by Inge Eriksen. """

PHASES = {
    "about": {
        "name": "Key Ideas",
        "fields": {
            "about": {
                "type": "text_area",
                "height": 200,
                "label": """What are the key ideas of this article?""",
                "value": "",
            }

        },
        "phase_instructions": "The user will offer 3 to 5 key ideas from the article. Please critically review their response for accuracy. Please offer friendly feedback if that suggest ideas that do not appear in the article.",
        "user_prompt": "{about}",
        "ai_response": True,
        "scored_phase": False,
        "allow_revisions": False,
        "max_revisions": 0,
        "allow_skip": False,
        "show_prompt": False,
        "read_only_prompt": False
    },
    "reflection": {
        "name": "Reflect",
        "fields": {
            "reflection": {
                "type": "text_area",
                "height": 300,
                "label": "How has this article changed your understanding of the cyberpunk genre?",
                "value":"",
            }
        },
        "phase_instructions": "The user reflect upon what they learned by reading the article. Critically evaluate their response to determine if they understand and have made a valid attempt to answer the question. If so, be supportive of their answer and their work on this exercise.",
        "user_prompt": "{reflection}",
        "ai_response": True,
        "scored_phase": False,
        "allow_revisions": True,
        "max_revisions": 2,
        "allow_skip": True,
        "show_prompt": False,
        "read_only_prompt": False
    }

}

def prompt_conditionals(prompt, user_input, phase_name=None):
    #TO-DO: This is a hacky way to make prompts conditional that requires the user to know a lot of python and get the phase and field names exactly right. Future task to improve it. 




    return prompt
    
selected_llm = "gpt-4o-mini"


LLM_CONFIGURATIONS = {
    "gpt-4o-mini": {
        "model": "gpt-4o-mini",
        "frequency_penalty": 0,
        "max_tokens": 1000,
        "presence_penalty": 0,
        "temperature": 1,
        "top_p": 1,
        "price_input_token_1M":0.150,
        "price_output_token_1M":.600
    },
    "gpt-4-turbo": {
        "model": "gpt-4-turbo",
        "frequency_penalty": 0,
        "max_tokens": 1000,
        "presence_penalty": 0,
        "temperature": 1,
        "top_p": 1,
        "price_input_token_1M":10,
        "price_output_token_1M":30
    },
    "gpt-4o": {
        "model": "gpt-4o",
        "frequency_penalty": 0,
        "max_tokens": 250,
        "presence_penalty": 0,
        "temperature": 1,
        "top_p": 1,
        "price_input_token_1M":5,
        "price_output_token_1M":15
    },
    "gemini-1.0-pro": {
        "model": "gemini-1.0-pro",
        "temperature": 1,
        "top_p": 0.95,
        "max_tokens": 1000,
        "price_input_token_1M":.5,
        "price_output_token_1M":1.5
    },
    "gemini-1.5-flash": {
        "model": "gemini-1.5-flash",
        "temperature": 1,
        "top_p": 0.95,
        "max_tokens": 1000,
        "price_input_token_1M":.35,
        "price_output_token_1M":1.05
    },
    "gemini-1.5-pro": {
        "model": "gemini-1.5-pro",
        "temperature": 1,
        "top_p": 0.95,
        "max_tokens": 1000,
        "price_input_token_1M":3.5,
        "price_output_token_1M":10.50
    },
    "claude-3.5-sonnet": {
        "model": "claude-3-5-sonnet-20240620",
        "max_tokens": 1000,
        "temperature": 1,
        "price_input_token_1M": 3,
        "price_output_token_1M": 15
    },
    "claude-opus": {
        "model": "claude-3-opus-20240229",
        "max_tokens": 1000,
        "temperature": 1,
        "price_input_token_1M": 15,
        "price_output_token_1M": 75
    },
    "claude-sonnet": {
        "model": "claude-3-sonnet-20240229",
        "max_tokens": 1000,
        "temperature": 1,
        "price_input_token_1M": 3,
        "price_output_token_1M": 15
    },
    "claude-haiku": {
        "model": "claude-3-haiku-20240307",
        "max_tokens": 1000,
        "temperature": 1,
        "price_input_token_1M": 0.25,
        "price_output_token_1M": 1.25
    }
}

SCORING_DEBUG_MODE = True
DISPLAY_COST = True

COMPLETION_MESSAGE = "You've reached the end! I hope you learned something!"
COMPLETION_CELEBRATION = False
