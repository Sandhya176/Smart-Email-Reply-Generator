# Smart-Email-Reply-Generator
This is an AI-powered Email Reply Generator I built using Spring Boot. It takes user input — an email message and the desired tone — and returns a professional reply using Google’s Gemini large language model. It’s helpful for users who want to quickly draft professional replies, especially in customer service or corporate communication.

The backend is developed in Java with Spring Boot. I used WebClient from Spring WebFlux to make API calls to the Gemini API.
____flow___:
1)User sends a POST request to /api/email/generate with:
  *emailContent – the original email
  *tone – the tone for the reply (e.g., polite, formal)
2)The controller accepts the request and passes it to the service.
3)The EmailGeneratorService:
   *Builds a prompt using the provided content and tone
   *Sends this prompt to Gemini’s API using WebClient
   *Parses the response from Gemini
   *Returns the generated email reply to the client
    *The response is a clean, professional reply, generated dynamically.
