# USSD App with Ngrok

This is a USSD (Unstructured Supplementary Service Data) application built using Node.js and Express. It allows users to avoid the illiteracy of not knowing the the laws and justice. The application is integrated with ngrok for local development and testing.

## Requirements

- Node.js
- Express
- ngrok

## Getting Started

1. Clone the repository:

   ```shell
   git clone https://github.com/patrickhag/ussd-app.git
   ```

2. Install the dependencies:

   ```shell
   npm install
   ```

3. Start the local server:

   ```shell
   npm start
   ```
3. Installing ngrok local server:

   [https://chat.openai.com/share/b194412b-d298-42c3-994d-4fcb5f5850d2]

4. Expose the local server using ngrok:

   ```shell
   ngrok http 9000
   ```

   The ngrok tool will generate a public URL that tunnels requests to your local server.

5. Configure the USSD callback URL:

   - Copy the ngrok URL provided by the previous command.
   - Open your mobile operator's USSD platform or simulator.
   - Set the USSD callback URL to `http://<ngrok-url>/ussd/callback`.

6. Test the USSD application:

   - Use USSD simulator like Africa's talking to dial the USSD code associated with your application.

## Customization

- To add more recent rules and laws, modify the code in the `router.post` handler of the Express application.

## License

This project is licensed under the MIT License. See the [LICENSE]([LICENSE](https://opensource.org/licenses/MIT)https://opensource.org/licenses/MIT) file for details.
