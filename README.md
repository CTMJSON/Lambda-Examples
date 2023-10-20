# Lambda-Examples
  /*
  // event exposes the activity object
    const call = event.activity; // call, text, chat, form, video, fax, etc...

  // context includes an http interface
  // GET request
    const get_url = 'https://api.your-service.com/some-endpoint';
    const {request, response, data} = await context.http_get(get_url);

  // POST request
    const body = JSON.stringify({key:'value'});
    const headers = {Authentication: 'Bearer ...', 'Content-Type':'application/json'};
    const post_url = 'https://api.your-service.com/some-endpoint';
    const { request, response, data } = await context.http_post(post_url, body, headers);

  //
  // event exposes
  // event.id       - a reference to this lambda function
  // event.activity - the call, text or form message that triggered this function, see event.activity.direction
  // event.options  - any additional user provided inputs e.g. custom actions can collect and populate this
  //

  // you can also use some helper methods to easily score or update an activity
  // await context.ctm.score('reportTag', 5, 400, true, new Date(), {fieldA: 'Super'});

  // or you can update the contact record fields associated to the activity
  // await context.ctm.update({name: 'Hello World', email: 'leads@example.com', custom_fields: {fieldA: 'Super'}});

  // both the http interface and the ctm interface return a Promise allowing you to wait for the methods to complete or
  // detect errors if they fail

  // if you are not using async await then you must be sure to call context.done() to signal the completion of your script, if you are using a promise use this in the
  // promise completion to ensure the code isn't terminated before the promise returns or within the response to a callback function.

  // Use askai to query a conversation
  // const email = await context.ctm.ask("What was the email address the caller provided?");
  // if (email) { await context.ctm.update({email: email}); }
  //

  // If you're using lambda function to route a phone call.
  context.done(null, {
    route: "ID Of Object you want to route to"
  })
  */
