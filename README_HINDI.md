# SaleDraft AI Hindi Text Reader

यह Python + FastAPI app PDF/Image से Hindi-English text निकालने के लिए है।

## क्या काम करेगा
- PDF में real text हो तो direct text निकलेगा।
- Scan PDF/Image हो तो OpenAI Vision से text पढ़ेगा।
- Hindi-English preserve mode: English को English, Hindi को Hindi रखने की कोशिश।
- Word (.docx) और TXT download।

## जरूरी बात
OpenAI API key चाहिए। API में image input/vision support होता है; इसलिए scan/image reading backend से चलेगी।

## GitHub पर कैसे डालें
1. GitHub खोलें → New repository.
2. Repository name: `saledraft-ai-reader`
3. Public/Private जो चाहें रखें.
4. Create repository.
5. Upload files में इस zip के सारे files upload करें.
6. Commit changes दबाएँ.

## Render पर deploy कैसे करें
1. render.com खोलें → New → Web Service.
2. GitHub repo connect करें.
3. Build Command: `pip install -r requirements.txt`
4. Start Command: `uvicorn app:app --host 0.0.0.0 --port $PORT`
5. Environment में add करें:
   - `OPENAI_API_KEY` = आपकी OpenAI API key
   - `AI_MODEL` = `gpt-4o-mini`
   - `MAX_PDF_PAGES` = `8`
6. Deploy दबाएँ.

## Google Sites में कैसे लगाएँ
Render deploy के बाद URL मिलेगा जैसे:
`https://saledraft-ai-reader.onrender.com`

Google Sites → Insert → Embed → By URL → Render URL paste करें.

या Embed code:
```html
<iframe src="https://YOUR-RENDER-URL.onrender.com" width="100%" height="1100" style="border:0;border-radius:18px"></iframe>
```

## सुरक्षा
API key कभी भी HTML/Google Sites code में paste मत करें। सिर्फ Render Environment Variables में रखें।
