# Event Registration

A registration form for an upcoming conference.

```xml
<body>
    <form>
        <section header="Attendee Details">
            <textfield key="fullName">Full Name</textfield>
            <textfield key="email">Email Address</textfield>
            <textfield key="company">Company</textfield>
        </section>
        <section header="Conference Options">
            <picker title="Ticket Type" key="ticketType" value="standard">
                <text tag="earlybird">Early Bird</text>
                <text tag="standard">Standard</text>
                <text tag="vip">VIP</text>
            </picker>
            <toggle key="workshop" value="false">Include Workshop Day</toggle>
        </section>
        <section header="Payment">
            <datepicker key="expiryDate" value="20251231T000000Z">Card Expiry</datepicker>
        </section>
        <section>
             <toggle key="terms" value="false">I agree to terms and conditions</toggle>
        </section>
    </form>
</body>
```
<img src="/Screenshots/Examples/Advanced/EventRegistration_1.png" width="250" alt="Screenshot">
