Here there are 2 project, the front and the backend

The backend is used to generate a signature, need to join to an existing meeting.

In the backend project, add you skd_key and sdl_Secret in the .env file, execute the comand :
npm run start

Make a POST request to http://localhost:4000 with meetingNumber(Required, the Zoom Meeting or Webinar Number) and role(Required, 0 to specify participant, 1 to specify host).
Example of request

{
  "meetingNumber": "123456789",
  "role": 0
}


example of response
{
  "signature": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzZGtLZXkiOiJhYmMxMjMiLCJtbiI6IjEyMzQ1Njc4OSIsInJvbGUiOjAsImlhdCI6MTY0NjkzNzU1MywiZXhwIjoxNjQ2OTQ0NzUzLCJhcHBLZXkiOiJhYmMxMjMiLCJ0b2tlbkV4cCI6MTY0Njk0NDc1M30.UcWxbWY-y22wFarBBc9i3lGQuZAsuUpl8GRR8wUah2M"
}



Rigth Now Im facing somes problems with the service response, returning an invalig signature, Im using postman instead of be able to ccreate a valid signature.