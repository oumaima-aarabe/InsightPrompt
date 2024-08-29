# InsightPrompt

### dependencies

langchain
openai
chainlit
chromadb
tiktoken
PyPDF2
pypdf
pandas
tabulate

#### 1. Text Processing
The system uses the RecursiveCharacterTextSplitter to process text from PDF files.
#### 2. Chain Setup
A chat prompt template (ChatPromptTemplate) is created using the chainlit library to handle user interactions.
#### 3. Chain Initialization
On chat start, the system initializes a retrieval-based question-answering chain (RetrievalQAWithSourcesChain).
#### 4. Message Handling
The script handles user messages using chainlit, interacting with the defined chain to retrieve answers based on the provided PDF text.
#### 5. Answer Display
Responses are constructed based on answers obtained from the question-answering chain, including source information and handling the display of final answers with associated sources.
#### 6. Callbacks and Session Management
Callbacks (AsyncLangchainCallbackHandler) are used to manage the flow of the chat and user sessions, storing metadata, text, and the initialized chain.
#### 7. File Processing
Uploaded PDF files are processed, and text is extracted from each page using PyPDF2. OpenAI embeddings are utilized for document retrieval.
