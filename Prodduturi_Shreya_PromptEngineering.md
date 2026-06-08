# Prompt Engineering Portfolio
Name: PRODDUTURI SHREYA
Date: 06-06-2026
LLM Used: ChatGPT 5.5

## Part 1: Prompt Design & Iteration
### 1.1 Scenario A: Technical Explanation
* Goal : Explain microservice to a 10-year-old.
* Initial Prompt (V1) : explain microservice for a beginner
* V1 Output:
        ----------------------------start--------------------------------------------
                Imagine you're building a food delivery app like Swiggy or Zomato.

        ### Before Microservices (Monolithic Application)

        Everything is inside **one big application**:

        * User Login
        * Restaurant Search
        * Order Management
        * Payments
        * Notifications

        All these features are packaged and deployed together.

        **Problem:**

        * A small change in Payments requires deploying the entire application.
        * If one module crashes, it can affect the whole system.
        * As the app grows, the code becomes difficult to maintain.

        ---

        ### With Microservices

        You split the application into smaller independent services:

        ```text
        Food Delivery App
        │
        ├── User Service
        ├── Restaurant Service
        ├── Order Service
        ├── Payment Service
        └── Notification Service
        ```

        Each service:

        * Has its own codebase.
        * Can be developed by a separate team.
        * Can be deployed independently.
        * Can have its own database.

        ---

        ### How They Communicate

        Suppose a user places an order:

        ```text
        User
        │
        ▼
        Order Service
        │
        ├──> Payment Service
        │
        └──> Notification Service
        ```

        The services communicate through APIs.

        Example:

        ```http
        POST /api/payments
        ```

        The Order Service calls the Payment Service to process the payment.

        ---

        ### Real-Life Analogy

        Think of a restaurant:

        * Chef → prepares food
        * Cashier → handles payments
        * Waiter → takes orders
        * Delivery Boy → delivers food

        Each person has a specific responsibility.

        Microservices work the same way—each service does **one job well**.

        ---

        ### Advantages

        ✅ Easier to maintain

        ✅ Faster development

        ✅ Independent deployment

        ✅ Better scalability

        Example:
        If Payment Service receives heavy traffic during a sale, you can scale only the Payment Service instead of the entire application.

        ---

        ### Challenges

        ❌ More services to manage

        ❌ Network communication can fail

        ❌ Debugging is harder because requests travel across multiple services

        ❌ Requires monitoring and logging tools

        ---

        ### Microservices in .NET

        A common .NET microservices setup might be:

        ```text
        API Gateway
            │
        ┌────┼────┐
        │    │    │
        ▼    ▼    ▼
        User  Order Payment
        API    API    API

        Each service:
        - ASP.NET Core Web API
        - Own Database
        - Docker Container
        ```

        Technologies often used:

        * ASP.NET Core
        * Docker
        * Kubernetes
        * RabbitMQ
        * Apache Kafka

        ### Interview Definition (3–4 Years Experience)

        > Microservices is an architectural style where an application is divided into small, independently deployable services, each responsible for a specific business capability. These services communicate through APIs or messaging systems and can be developed, deployed, and scaled independently.

        As a .NET developer, understanding microservices is important because many modern enterprise applications are built using this architecture.

    --------------------END----------------------
* Refined Prompt (V2) : you are a school teacher. can you now explain same to a 10year old?
* V2 Output 
        -----------------START--------------------------
        Sure! 😊

        Imagine your school is organizing a big annual day event.

        ### One Big Helper (Monolithic App)

        Suppose **one student** has to do everything:

        * Invite guests
        * Arrange chairs
        * Manage music
        * Distribute snacks
        * Take attendance

        If that student gets sick or makes a mistake, the whole event can be affected.

        ---

        ### Many Small Helpers (Microservices)

        Now imagine the teacher gives each job to a different student:

        👧 Student 1 → Invites guests

        👦 Student 2 → Arranges chairs

        👧 Student 3 → Controls music

        👦 Student 4 → Distributes snacks

        👧 Student 5 → Takes attendance

        Each student has **one responsibility**.

        If the music student is absent, the others can still do their jobs.

        ---

        ### How They Work Together

        When guests arrive:

        1. Attendance student marks their names.
        2. Chair student helps them find seats.
        3. Music student starts the songs.
        4. Snack student gives refreshments.

        Everyone works on their own task, but together they make the event successful.

        ---

        ### That's Exactly What Microservices Are!

        A big computer program is divided into many small programs.

        Each small program:

        * Does one job.
        * Works independently.
        * Talks to other programs when needed.

        For example, in a food delivery app:

        🍔 Food Service → Shows restaurants

        👤 User Service → Manages accounts

        💳 Payment Service → Handles money

        📦 Order Service → Tracks orders

        Each service has its own job, just like the students helping with the school event.

        ### Simple Definition for a 10-Year-Old

        **Microservices are like a team of helpers where each helper does one special job, and all the helpers work together to complete a big task.** 😊

        --------------------END----------------------
* Final Prompt (V3) : assume this 10year old has difficulty in understanding basic concepts. Now can you explain?
* Final Output : 
        --------------------START----------------------
        Of course! Let's make it even simpler. 😊

        Imagine you have a toy box full of LEGO blocks.

        You want to build a house.

        If **one person** tries to do everything:

        * Find the blocks
        * Build the walls
        * Build the roof
        * Make the doors
        * Make the windows

        it takes a long time.

        Now imagine **five friends** help you:

        * Friend 1 finds the blocks.
        * Friend 2 builds the walls.
        * Friend 3 builds the roof.
        * Friend 4 makes the doors.
        * Friend 5 makes the windows.

        Each friend does **just one small job**.

        When everyone finishes their small job, you put all the pieces together and get a complete house.

        ### Microservices are like those friends.

        A big computer program is broken into many small programs.

        Each small program does **one small job**.

        For example, when you order a pizza online:

        🍕 One small program remembers who you are.

        🍕 One small program takes your order.

        🍕 One small program takes your payment.

        🍕 One small program sends a message saying, "Your pizza is coming!"

        All these small programs work together, just like your friends building the LEGO house.

        ### Super Short Version

        **Microservice = One small helper that does one small job.**

        Many small helpers working together = One big application. 😊

        --------------------END----------------------

### 1.1 Scenario B: Professional Email
* Goal : Draft an email declining a job offer politely while expressing continued interest in the company
* Initial Prompt (V1) : Draft an email declining a job offer politely while expressing continued interest in the company
* V1 Output:
        ----------------------------start--------------------------------------------
        Here's a polite and professional email template:

        Subject: Thank You for the Offer

        Dear [Hiring Manager's Name],

        Thank you very much for offering me the position of [Job Title] at [Company Name]. I sincerely appreciate the time and effort that you and the team invested throughout the interview process.

        After careful consideration, I have decided to decline the offer at this time. This was not an easy decision, as I was genuinely impressed by the company's culture, vision, and the professionalism of everyone I met during the process.

        While I have chosen to pursue a different opportunity that aligns more closely with my current career goals, I remain very interested in [Company Name] and would welcome the possibility of exploring opportunities together in the future.

        Thank you again for your confidence in my abilities and for extending this offer. I wish you and the team continued success, and I hope our paths may cross again.

        Kind regards,

        [Your Full Name]
        [Phone Number]
        [Email Address]

        If you'd like, I can also make it:

        * **warmer and more personal**
        * **short and concise**
        * **tailored for declining due to salary, location, health, or another offer**.


    --------------------END----------------------
* Refined Prompt (V2) : can you draft the mail and make it shorter and warmer
* V2 Output 
        -----------------START--------------------------
        **Subject:** Thank You for the Opportunity

        Dear [Hiring Manager's Name],

        Thank you so much for offering me the opportunity to join [Company Name]. I truly appreciate the time and effort you and the team invested throughout the interview process.

        After careful consideration, I have decided to decline the offer at this time. This was a difficult decision, as I was genuinely impressed by the team, the company, and the work being done at [Company Name].

        I sincerely appreciate the opportunity and hope our paths cross again in the future.

        Wishing you and the team all the very best.

        Warm regards,
        [Your Name]
        --------------------END----------------------
* Final Prompt (V3) : assume you are a professional career coach. Write a polite email declining a job offer because I accepted another opportunity. And say you are happy and could not join at the moment but interested in future opportunities. Keep the tone professional and warm
* Final Output : 
        --------------------START----------------------
        This version keeps the tone warm, appreciative, and professional while clearly communicating your decision:

        Subject: Thank You for the Opportunity

        Dear [Hiring Manager's Name],

        Thank you very much for offering me the position at [Company Name]. I sincerely appreciate the time and effort you and the team invested throughout the interview process.

        After careful consideration, I have decided to move forward with another opportunity that I have accepted. As a result, I will not be able to join [Company Name] at this time.

        This was not an easy decision, as I thoroughly enjoyed getting to know the team and learning more about the exciting work being done at your organization. I am genuinely grateful for the opportunity and honored to have been considered.

        I hold [Company Name] in high regard and would welcome the chance to stay connected and explore potential opportunities together in the future.

        Thank you again for your understanding, and I wish you and the team continued success.

        Warm regards,

        [Your Name]

        This is the type of email that leaves the door open for future opportunities while remaining respectful and concise.
        --------------------END----------------------
### 1.1 Scenario C: Creative Content
* Goal : Generate a creative marketing tagline for a new eco-friendly water bottle brand
* Initial Prompt (V1) : can you suggest me a tagline for new eco friendly water bottle brand
* V1 Output:
        ----------------------------start--------------------------------------------
        Here are some tagline ideas for an eco-friendly water bottle brand, grouped by style:

        ### Nature-Focused

        * **Pure Water. Pure Planet.**
        * **Sip Green, Live Clean.**
        * **Hydrate Naturally.**
        * **Drink Better. Leave Less.**
        * **Every Sip Supports Earth.**

        ### Modern & Premium

        * **Sustainability in Every Sip.**
        * **Designed for Water. Made for Tomorrow.**
        * **Refresh Responsibly.**
        * **Smart Hydration. Cleaner Future.**
        * **Carry Change. Drink Pure.**

        ### Short & Catchy

        * **Refill. Reuse. Repeat.**
        * **Sip. Save. Sustain.**
        * **Bottle the Future.**
        * **Drink Green.**
        * **Hydrate with Purpose.**

        ### Impact-Driven

        * **One Bottle. Thousands of Plastic Bottles Avoided.**
        * **Choose Reuse. Choose Earth.**
        * **Hydration Without Harm.**
        * **Good for You. Better for the Planet.**
        * **Small Bottle. Big Difference.**

        ### Premium Indian Market Style

        * **Pure Hydration, Responsible Living.**
        * **Every Drop Matters.**
        * **Earth-Friendly. Life-Ready.**
        * **Inspired by Nature, Built for Life.**
        * **The Sustainable Way to Stay Hydrated.**

        If you share your brand name and target audience (premium, sports, kids, office professionals, luxury, etc.), I can create taglines tailored specifically to the brand.


    --------------------END----------------------
* Refined Prompt (V2) : target audience is for everyone, and my goal is anybody can afford it and has good quality
* V2 Output 
        -----------------START--------------------------
        Since your brand is for **everyone**, focuses on **affordability**, **good quality**, and **eco-friendliness**, the tagline should be simple, memorable, and inclusive.

        ### Top Recommendations

        1. **Better for You. Better for Earth.**
        2. **Quality You Trust. Price You Love.**
        3. **Sustainable Hydration for Everyone.**
        4. **Good for Your Wallet. Great for the Planet.**
        5. **Eco-Friendly. Everyday Friendly.**
        6. **Clean Water. Cleaner Future.**
        7. **Affordable. Durable. Sustainable.**
        8. **Hydrate Smarter, Live Greener.**
        9. **A Better Bottle for Every Day.**
        10. **Quality Hydration Within Reach.**

        ### Short, Brandable Taglines

        * **Sip Green.**
        * **Drink Better.**
        * **Choose Reuse.**
        * **Pure. Simple. Sustainable.**
        * **Hydrate Responsibly.**
        * **Made to Last. Made to Care.**

        ### If You Want a Strong Brand Positioning

        These communicate your mission clearly:

        * **Sustainable Hydration for Every Home.**
        * **Making Eco-Friendly Living Affordable.**
        * **Quality Bottles, Cleaner Planet.**
        * **Because Everyone Deserves a Better Bottle.**
        * **Affordable Sustainability, One Sip at a Time.**

        My strongest picks for a mass-market brand would be:

        🏆 **Eco-Friendly. Everyday Friendly.**
        🏆 **Because Everyone Deserves a Better Bottle.**
        🏆 **Affordable Sustainability, One Sip at a Time.**
        🏆 **Quality Hydration Within Reach.**

        These are easy to understand, appeal to a broad audience, and highlight both affordability and sustainability.


        --------------------END----------------------
* Final Prompt (V3) : you are a senior branding expert and have 10+ years experience in this field. Create short, memorable taglines for a premium eco-friendly water bottle brand. Focus on sustainability, affordability, and innovation. 
* Final Output : 
        --------------------START----------------------
        For a **premium eco-friendly water bottle brand**, the strongest taglines are usually **2–4 words**, easy to remember, and emotionally meaningful. They should hint at sustainability and innovation without sounding preachy.

        ### Premium & Memorable

        * **Sip the Future**
        * **Hydrate Smarter**
        * **Pure by Design**
        * **Drink Forward**
        * **Refill Tomorrow**
        * **Sustain Every Sip**
        * **Future in Hand**
        * **Purpose in Every Sip**
        * **Smart. Pure. Sustainable.**
        * **Designed to Reuse**

        ### Premium + Sustainable

        * **Luxury Meets Sustainability**
        * **Elegance, Responsibly**
        * **Refined for Tomorrow**
        * **Sustainable by Nature**
        * **Made for More**
        * **Greener Every Day**
        * **Premium. Planet. Purpose.**
        * **Crafted for Change**

        ### Affordable + Sustainable

        * **Better Bottles for All**
        * **Sustainability Within Reach**
        * **Quality, Not Waste**
        * **Everyday Sustainability**
        * **Affordable. Sustainable. Better.**
        * **Good for All**
        * **Smart Choice, Lasting Impact**

        ### Innovation-Focused

        * **Innovation You Can Sip**
        * **The Next Sip**
        * **Reimagining Hydration**
        * **Hydration, Reinvented**
        * **Designed for Better**
        * **Where Innovation Flows**
        * **Future-Proof Hydration**

        ### Branding Agency–Style Options

        These are the kind of taglines that tend to test well because they are concise, distinctive, and scalable:

        1. **Sip the Future**
        2. **Drink Forward**
        3. **Hydrate Smarter**
        4. **Purpose in Every Sip**
        5. **Refill Tomorrow**
        6. **Pure by Design**
        7. **Sustain Every Sip**
        8. **Designed for Better**
        9. **Better Bottles for All**
        10. **Future in Hand**

        If your brand aims to become the **"Tesla of water bottles"** (innovation-led), I'd choose **"Sip the Future."**

        If it aims to become the **"Apple of sustainable hydration"** (premium + design), I'd choose **"Pure by Design."**

        If it aims to be a **mass-market brand with broad appeal**, I'd choose **"Better Bottles for All."**

        --------------------END----------------------
### 1.2 Iteration Documentation

* Scenario A – Technical Explanation 
    | Version | Prompt | What Changed | Why This Improved the Output |
    |----------|----------|----------|----------|
    | V1 | Explain microservice for a beginner. | N/A | N/A |
    | V2 | You are a school teacher. Can you explain the same concept to a 10-year-old? | Added a role (school teacher) and specified the target audience (10-year-old). | The explanation became simpler and used a school-event analogy that children can easily relate to. |
    | V3 | Assume this 10-year-old has difficulty understanding basic concepts. Now can you explain? | Added additional context about the learner's comprehension level. | The explanation became even simpler, using a LEGO-building analogy and shorter sentences, making the concept easier to understand. |
    
* Scenario B – Professional Email
    | Version | Prompt | What Changed | Why This Improved the Output |
    |----------|----------|----------|----------|
    | V1 | Draft an email declining a job offer politely while expressing continued interest in the company. | N/A | N/A |
    | V2 | Can you draft the email and make it shorter and warmer? | Added requirements for brevity and a warmer tone. | The email became more concise and warmer while remaining professional. |
    | V3 | Assume you are a professional career coach. Write a polite email declining a job offer because I accepted another opportunity. Mention that I appreciate the offer, cannot join at the moment, but am interested in future opportunities. Keep the tone professional and warm. | Added a role (professional career coach) and detailed context about the reason for declining. | The email became more tailored, clearly communicated the decision, and expressed interest in future opportunities. |

* Scenario C – Creative Content
    | Version | Prompt | What Changed | Why This Improved the Output |
    |----------|----------|--------------|------------------------------|
    | V1 | Can you suggest me a tagline for a new eco-friendly water bottle brand? | N/A | N/A |
    | V2 | Target audience is for everyone, and my goal is anybody can afford it and has good quality. | Added target audience and brand positioning details. | Taglines are now more relevant to a broader audience and better communicate affordability and quality. |
    | V3 | You are a senior branding expert with 10+ years of experience. Create short, memorable taglines for a premium eco-friendly water bottle brand. Focus on sustainability, affordability, and innovation. | Added a role (branding expert) and specified focus areas: sustainability, affordability, and innovation. | The taglines became more strategic, professional, and aligned with established branding practices. |

### 1.3 Role and Context Analysis
    In Scenario A and Scenario C, role assignment improved the outputs. Assigning role as a school teacher helped in providing age-appropriate examples and in simple language. Assigning role as Senior Branding expert produced more profeesional and tailored response. Assigning role as Carrer coach gave professional response. And providing more context to the questions helped in getting more relevant and accurate answers and aligned with the intended purpose.

-------------------------------------------------------------------------------------------------------------------

## Part 2: Temperature & Parameter Control
### 2.1 Temperature Experimentation
        * Topic : What is photosynthesis?
        * Prompt 1 (Low Temperature) : Explain what photosynthesis is? Be precise and consistent
        * Output :
                --------- START ----------
                **Photosynthesis** is the biological process by which plants, algae, and certain bacteria convert light energy into chemical energy stored in sugars.

                ### Core Definition
                Using energy from sunlight, photosynthetic organisms transform **carbon dioxide (CO₂)** and **water (H₂O)** into **glucose (C₆H₁₂O₆)** and **oxygen (O₂)**.

                The overall equation is:

                genui{"math_block_widget_always_prefetch_v2":{"content":"6CO_2 + 6H_2O + light\\ energy \\rightarrow C_6H_{12}O_6 + 6O_2"}}

                ### Where It Occurs
                In plants, photosynthesis occurs mainly in the **chloroplasts** of leaf cells. Chloroplasts contain **chlorophyll**, a pigment that absorbs light, especially in the blue and red regions of the spectrum.

                ### Two Main Stages

                #### 1. Light-Dependent Reactions
                - Occur in the thylakoid membranes of chloroplasts.
                - Light energy is absorbed by chlorophyll.
                - Water molecules are split (**photolysis**).
                - Oxygen is released as a byproduct.
                - Energy carriers **ATP** and **NADPH** are produced.

                #### 2. Calvin Cycle (Light-Independent Reactions)
                - Occurs in the chloroplast stroma.
                - ATP and NADPH from the first stage are used.
                - Carbon dioxide is fixed into organic molecules.
                - Sugars are synthesized, ultimately leading to glucose production.

                ### Why Photosynthesis Matters
                Photosynthesis:
                1. Produces most of the oxygen in Earth's atmosphere.
                2. Forms the base of nearly all food chains.
                3. Converts solar energy into chemical energy available to living organisms.
                4. Removes carbon dioxide from the atmosphere and stores carbon in biomass.

                ### Precise Summary
                Photosynthesis is the process by which photosynthetic organisms use light energy to convert carbon dioxide and water into energy-rich carbohydrates, releasing oxygen as a byproduct. The light-dependent reactions capture and store energy, and the Calvin cycle uses that energy to build sugars from carbon dioxide.
                --------- END ------------
        * Prompt 2 (Medium Temperature) : Explain what photosynthesis is?
        * Output :
                --------- START ----------
                **Photosynthesis** (Photosynthesis) is the process by which green plants, algae, and some bacteria make their own food using sunlight.

                ### 🌱 What happens during photosynthesis?

                ![Image](https://images.openai.com/static-rsc-4/CWTedKVQGoH2asQ6HNdCbT5Ke53xOT-Y4ctEz1L151Oym5o4WUYM2TTVEiODrNwxSlCs6K3RoU4UwlqcU6Wno_VGAHllIST0MDo0C4LEtUipTatyZtTb_9CImItqBHUDbQgVjqKuba-Zu6NNIotCtKTTht1TpScvMhw5PX89MfCPh38zFEKWz7Q8LTIuI772?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/GBZAebzVNNUn6SiGIHfnJEpkbLIQqiFXgpVEpSnX4oyRz3ds87Bk1L_iZNStWbyAYsVu9fekpAClii7Nn0IKUO1VjCJ_x6T896d7tJsPVxUe2WLLANMbXviPNeVTEDqT4IN19IOrDzVkT5Gf3X7gnqNqYxCz6SdzXbRd5NNpokdmz3A6vpKJfcvHxttNg_uM?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/SO5R3XzaYk7njBNEaGma1RJVsR3e7oKvka69TDARM9hgh4lKFb0JY6FFyaa-IRJLY1f3G4q1iuc0ctognY2SD9io3BVyq8cIr60sgApHnGhxowsk-xw3oLXXeLG9hW2fb04jZN3A_veBx1dhBKNvRpeNCC_BweNAclIWhUpcNMi24lpKRGNUgzU6KLDumP5h?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/zipNn9pfzODP9PfPFZw0yh_e_85DjKLaTWW915UlY9SLM2KkjqReLz-ktAiHQ-NYnmPC-WiuU-Ut6bUBLGzZH0ndx77kLr8SXJt_wy3_jvisz1c4M0ESm2sEweZ-y__4DaAF9-OImsjhmQ3OD8scEviwaE8aK4ZnZWgekUKCVEvFVn7LdO0P8eguT6ScebAU?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/DWsRYP2kTZb3Hc695s6qcv9s4Ozngx4UeEORrPKh5zDdIV0caGzM220qzYxxSdnG5JVRra-fKagYZCll7N2ty_g6U-inDGA2kfY6XqaMCI_255nyGPwDZscdT6LxQXZezrqdp5RHmdJNi9SPCXdmRR1fg0HsDvo2AQeXmKbtjizfibo2Lrhu1cK13zJQ4MVz?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/d2cscF3fIQw6LWbi3w0A6N6_iNIF4Ii7sbIsu02MiZm9qi-CqMJ4QWFYOngbkQipBTLXsjJTXrHqgDz9TXRV2WJqKDHPAn8oH_RZWRE_mYy3ju5ivQMoc3Emn_iOFbUxaPgi19Gz-zA0WCGheZRXC1kkdy3FauXHm1HLA3awDwPlBCV-LHppief-F0XSEIU1?purpose=fullsize)

                In simple terms, photosynthesis works like this:

                * Plants take in **carbon dioxide (CO₂)** from the air through their leaves
                * They absorb **water (H₂O)** from the soil through their roots
                * Using energy from **sunlight**, they convert these into:

                * **Glucose (a type of sugar)** — their food
                * **Oxygen (O₂)** — released into the air

                ### ☀️ The basic equation

                Carbon dioxide + water + sunlight → glucose + oxygen

                ### 🌿 Why it’s important

                Photosynthesis is essential for life on Earth because:

                * It produces **oxygen** that animals (including humans) breathe
                * It forms the **base of the food chain** (plants feed everything else, directly or indirectly)
                * It helps regulate **carbon dioxide levels** in the atmosphere

                In short, photosynthesis is how plants turn sunlight into energy—and it’s one of the main reasons life on Earth can exist at all.
                --------- END ------------
        * Prompt 3 (High Temperature) : Explain what photosynthesis is? Be creative and explore diverse ideas
        * Output : 
                --------- START ----------
                Imagine Earth as a vast solar-powered city.

                The Sun is the energy company. Plants are the master engineers. Leaves are millions of tiny green factories. And photosynthesis is the process that turns sunlight into food.

                At its core, photosynthesis is how plants, algae, and some bacteria capture light energy and store it as chemical energy in sugars.

                The basic recipe looks like this:

                6CO_2 + 6H_2O + light\ energy \rightarrow C_6H_{12}O_6 + 6O_2

                In words:

                * Plants take in carbon dioxide from the air.
                * They absorb water from the soil.
                * Sunlight provides energy.
                * They produce glucose (a sugar that stores energy).
                * Oxygen is released as a byproduct.

                ## A Different Way to Think About It

                ### Photosynthesis as Solar Battery Manufacturing

                A solar panel captures sunlight, but it doesn't store much energy itself.

                Plants do something even more impressive:

                1. Capture sunlight.
                2. Convert it into chemical bonds.
                3. Store that energy in molecules.

                A tree is essentially a giant living battery built from sunlight.

                The wood in a tree trunk is "frozen sunlight" accumulated over years.

                ---

                ### Photosynthesis as Time Travel

                When you burn firewood, you're releasing sunlight that struck Earth years ago.

                When you burn coal or oil, you're releasing sunlight that ancient plants captured millions of years ago.

                In a sense, fossil fuels are ancient photosynthesis stored underground.

                ---

                ### Photosynthesis as Planetary Architecture

                Photosynthesis doesn't merely feed plants—it built much of the living world.

                The energy in:

                * fruits,
                * vegetables,
                * grains,
                * animals,
                * humans,

                can often be traced back to photosynthesis.

                Even a lion depends on photosynthesis indirectly. The lion eats a zebra, the zebra eats grass, and the grass captures sunlight.

                Most food chains begin with photosynthetic organisms.

                ---

                ### Photosynthesis as Earth's Oxygen Factory

                ![Image](https://images.openai.com/static-rsc-4/LeedaYnbBiGVbd-CkwG2DpPIobeZolbEJGeF9Rn-7n3BGMGik44u8sHEt9buUTLUG1a5W4Tt97lv5tjemnTNKFb35CV0wrviYng0JBw2yf2W7dTYHZHJ9ePmon-vutFtcX6eZen6n_HNLFMSVxdtiuMouv_Nwqe4VYWJFOpjNqrD5bDWVOEVTtuSztlvZrRf?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/7OyslLgQ2W3GCS5qhVyBeHZwjPsf5uDEiaJA_oDWsWZK0ow3v35dldcP__35bh6n6zhMoLtX8MfTFciEuaxx7PywibmVu8t8oTQllSXD9isYL-yoJD6KFWqUpQtnPm1y4_qcC4b2xuw8VFr8yKL6g7eQ4s-g9i3l9qpHlSi8La8kd0hT3mCaJ4O1_iV3KRrS?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/jWtsJNtg8IINyORXdnV0ia9bnBrUr1OjpCo6kn8VTj5rGoVg8uJSEePxDgm5Nw0AakjwVBWi_w1vYxBgpxhHUm7OEppBGD7O2FQXz8EFFYZES1jt8JxGMx09GEEHffEsOtVajmMkAegqzj8VMicrDlGOLJyDXB4hDScV3F2S7VBafvyhiihrK7ibe_FFp4LD?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/kpeLUgSXrJTQ59zKw0Hh4dtyKIYwgn8IfOEm3poK1Tj2EItbP7vg1quU_Lk5tPl62z4pUu1_wLJ2-Whs2EBvLc9zCNBrw_fO6jhn-6JS_c7AXZwc4BDkX2xy9NPZnsU6D11LuWlNQDQD6_b4qWs8bY3k3ORwmcCqz1Xiq5OiVJ6kE4biGJjaXOuql4qVU6lX?purpose=fullsize)

                Before photosynthetic organisms evolved, Earth's atmosphere contained very little oxygen.

                Ancient microbes began producing oxygen through photosynthesis billions of years ago. Over immense stretches of time, this transformed the atmosphere and enabled complex life to evolve.

                One of the most consequential events in Earth's history was the Great Oxidation Event.

                Every breath you take is connected to that ancient innovation.

                ---

                ### Photosynthesis as a Global Conversation

                Plants are constantly exchanging materials with their environment:

                * They "inhale" carbon dioxide.
                * They "drink" water.
                * They "harvest" light.
                * They "exhale" oxygen.

                The atmosphere, oceans, soil, and living organisms are all linked through this exchange.

                Photosynthesis is one of the key engines of the global carbon cycle.

                ---

                ### The Tiny Machines Inside Leaves

                Inside plant cells are structures called chloroplasts.

                ![Image](https://images.openai.com/static-rsc-4/ktW1zrZSWhr1nEb2Uexej8is0Vw3aRjOL9bJztsTEDDhO6R9HjLXjVtVx_JuoZz4MzkW1d8A3KiP3O__W5UOfPFiXp0VqbXttXjaiWdWwykJ4pdpFe16S6Hi6jzIfwhD-ncsmjpI2CmyEetNlXvfk0bYGwt6PHEGKQEypd3iKWOLq5UV_eUbuUnJbBadmZqO?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/sTGD4BkDrWy0Cx3HBBTfkvOdrbvGl-1501to-YpFO8xl81zZH5lZze64PE8UcJBmtGxQZLNvg9JS97UJ2kDL9JUsV2-vYRXgsi9kR9lAY0PJuJTOgUKTRIjxbtBgyiRoKWRGsz6NCSQVpikPAybmlgIkDiKTxMC2Z42_lHvrlK_4rVbw2JyW8vcFuDxLWfsl?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/1aGa_OTujxBvDQxL04-Js6WWUlwI5nQjN130Zt9d8T5RbN--jIAxIEkRV1qjTE3Ix_4G2SS7-Zc43YLzLmSpeFHbsMPVR5-U-rIhHYwhkSj0P1il26yrjB5apxWPS_pz3hzHfmr1ARBRKnt3VOMBB6UR_pj9Ge-uhFz8ysowzBiY0v_i2ZEJw4MBcHxzFX6-?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/8GzWN16FB8WgyeY4zaHZp9w3ruTl1v1NEQK6lG3xfcYjPkr00FrBIuix6WftmGXqGVQU9Ypp6pGW_FSRbULi9a6kKqXuufHAD6JNKgoRURQ8SQ5hyGW7qMINkOt_LfFJJyoT6vGkWA2iLMZ_lkcvOdKVjAkjkIQwdbFjd8wAN2wdQJiAdAoC_WTJzqxC9z-I?purpose=fullsize)

                ![Image](https://images.openai.com/static-rsc-4/eaYiy4aoucMAPV7fGZDRIU5JqBKPKC_ciojAt01x3DCiu7E9rBIawKFJfQQKD5LrS6TNmeUnx5VOjTCxNbBfkygw6W435UD6kPovjxkUJ3apxTIO-zM5IuXhwPta2xOoeAV47uP8Hm8onanUxtBOS9NyG8TfYVYWoM5XDpoBHxPK-5DizSGmcXrTfIThwDNf?purpose=fullsize)

                These chloroplasts contain chlorophyll, the green pigment that absorbs light.

                Chlorophyll doesn't absorb all colors equally. It reflects green light more than many other wavelengths, which is why most plants appear green to us.

                ---

                ### A Cosmic Perspective

                Photosynthesis is remarkable because it allows life to feed directly on starlight.

                Nearly every ecosystem on Earth depends on organisms that can capture energy arriving from our star, the Sun.

                The Sun shines. Plants catch a fraction of that light. The captured energy becomes leaves, forests, crops, ecosystems, and ultimately entire civilizations.

                Seen this way, photosynthesis is not just a biological process—it's the mechanism that connects a star 150 million kilometers away to every meal, forest, and breath on Earth.

                In a single sentence:

                **Photosynthesis is the art by which life turns sunlight into living matter.** ☀️🌱
                --------- END ------------
### 2.2 Analysis & Recommendations
        * When would you use low temperature? (Give 2 specific use cases)
                * I would use for academic content where factual correctness is essential
                * For professional documentation and medical related fields that require precise and accurate information.
        * When would you use high temperature? (Give 2 specific use cases)
                High temperature can be used for creativity related use cases like:
                * Story telling
                * Innovative solutions
        * Which temperature worked best for your chosen task and why?
                * Medium temperature worked best for my chosen task as it maintained factual accuracy and explanation was clear and concise. As it not too technical and too creative. Medium temperature balanced all aspects of explanation well.

-------------------------------------------------------------------------------------------------------------------

## Part 3: Strategic Prompting Techniques

### 3.1 Chain-of-Thought Prompting

### Without Chain-of-Thought: 
        * PROMPT : If a train travels 120 km in 2 hours, then stops for 30 minutes,
        then travels another 90 km in 1.5 hours, what is its average speed for
        the entire journey?
        * Show the LLM output : 52.5 km/h
### With Chain-of-Thought: Write a prompt that instructs the LLM to think step-by-step
        * Example instruction: Now think step by step and show me answer
        * Show the LLM output with reasoning:
                Distance traveled:

                * First part: 120 km
                * Second part: 90 km
                * **Total distance = 120 + 90 = 210 km**

                Time taken:

                * First part: 2 hours
                * Stop: 30 minutes = 0.5 hours
                * Second part: 1.5 hours
                * **Total time = 2 + 0.5 + 1.5 = 4 hours**

                Average speed:

                \text{Average Speed}=\frac{210}{4}

                **Average speed = 52.5 km/h**.

### Comparison: In 3-4 sentences, explain:
        * How the outputs differed : Outputs differed in amount of explanation. Without chain of thought,  model gave direct answer. With chain of thought, model gave detailed explanation of how it is able to give the answer.
        * Why chain-of-thought helps with complex reasoning : Helps in understanding by giving step by step detailing and improves transparency by showing how the conclusion was reached. 
        * One limitation you observed : longer responses and sometimes too much explanation

### 3.2 Few-Shot Prompting

Task: Create a sentiment classifier using few-shot prompting
Your Mission: Teach the LLM to classify customer reviews as Positive, Negative, or Neutral

### Step 1: Zero-Shot Attempt (5 points)
        * Prompt : 
                classify sentiment for below reviews
                "The product arrived damaged and customer service was unhelpful."
                "Works as expected, nothing special but does the job."
                "Absolutely love this! Best purchase I've made all year!"
                "The quality is okay but slightly overpriced for what you get."
                "Terrible experience, would not recommend to anyone."
        * Output :
                Here is a simple sentiment classification for each review:

                | Review                                                            | Sentiment                               |
                | ----------------------------------------------------------------- | --------------------------------------- |
                | "The product arrived damaged and customer service was unhelpful." | **Negative**                            |
                | "Works as expected, nothing special but does the job."            | **Neutral**                             |
                | "Absolutely love this! Best purchase I've made all year!"         | **Positive**                            |
                | "The quality is okay but slightly overpriced for what you get."   | **Neutral** (slightly negative leaning) |
                | "Terrible experience, would not recommend to anyone."             | **Negative**                            |

                As a labeled dataset:

                ```text
                1. Negative
                2. Neutral
                3. Positive
                4. Neutral
                5. Negative
                ```

### Step 2: Few-Shot Attempt (10 points)
        * Prompt :
                classify sentiment for below reviews
                "The product arrived damaged and customer service was unhelpful."
                "Works as expected, nothing special but does the job."
                "Absolutely love this! Best purchase I've made all year!"
                "The quality is okay but slightly overpriced for what you get."
                "Terrible experience, would not recommend to anyone."
                below are the example classification:
                Review: "This product exceeded my expectations!"
                Sentiment: Positive

                Review: "Completely broke after one week of use."
                Sentiment: Negative

                Review: "It's fine, does what it says on the box."
                Sentiment: Neutral
        * Output :
                Review: "The product arrived damaged and customer service was unhelpful."
                Sentiment: **Negative**

                Review: "Works as expected, nothing special but does the job."
                Sentiment: **Neutral**

                Review: "Absolutely love this! Best purchase I've made all year!"
                Sentiment: **Positive**

                Review: "The quality is okay but slightly overpriced for what you get."
                Sentiment: **Neutral**

                Review: "Terrible experience, would not recommend to anyone."
                Sentiment: **Negative**


### Step 3: Analysis
        * Comparison Table : 
                | Review # | Zero-Shot Result | Few-Shot Result | Correct Label | Improved? |
                | -------- | ---------------- | --------------- | ------------- | --------- |
                | 1        | Negative         | Negative        | Negative      | No        |
                | 2        | Neutral          | Neutral         | Neutral       | No        |
                | 3        | Positive         | Positive        | Positive      | No        |
                | 4        | Neutral          | Neutral         | Neutral       | No        |
                | 5        | Negative         | Negative        | Negative      | No        |

        * Analysis : 
                Few-shot prompt did not improve the classification results because zero-shot already correctly identified the sentiment of all five reviews. However, few-shot prompting is most useful when tasks are ambiguous and complex.Few-shot prompting helps the model better understand the expected output format and decision criteria, often improving accuracy and consistency on more challenging datasets.
-------------------------------------------------------------------------------------------------------------------
## Part 4: Responsible AI & Limitations
### 4.1 Testing for Hallucinations
        * Prompt : What is the purpose of the Kaveri Atmospheric Index, and how is it calculated?
        * Response : 
                I’m not aware of any widely recognized meteorological, environmental, or hydrological measure called the **“Kaveri Atmospheric Index.”** I checked for references and could not find a standard index by that name in scientific or operational use. The search results instead returned established atmospheric indices such as the **K-index** used in meteorology and various studies of the entity["place","Kaveri River","Southern India river basin"] basin. citeturn1search24turn1search25

                It’s possible that:

                1. You may mean the **K-index (meteorology)**, which estimates thunderstorm potential.
                2. The term is from a specific research paper, government report, or local project related to the Kaveri/Cauvery basin.
                3. The name may have been abbreviated or misremembered.

                If you mean the **K-index**, its purpose is to assess atmospheric instability and the likelihood of thunderstorms. It is calculated from temperatures and dew points at specific pressure levels:

                genui{"math_block_widget_always_prefetch_v2":{"content":"K=(T_{850}-T_{500})+T_{d850}-(T_{700}-T_{d700})"}}

                where:
                - \(T_{850}, T_{700}, T_{500}\) are temperatures at 850, 700, and 500 hPa,
                - \(T_{d850}, T_{d700}\) are dew-point temperatures at 850 and 700 hPa. Higher values generally indicate greater thunderstorm potential. citeturn1search24turn1search27

                If you have a source, document, or context where “Kaveri Atmospheric Index” is mentioned, send it to me and I can explain its exact purpose and calculation.

        * Did it Hallucinate : Admitted uncertainity
        * Updated Prompt : If you don't know, please say so rather than guessing
        * Response : 
                You're right.

                I should have said: **I don't know what the "Kaveri Atmospheric Index" is.** I am not aware of any widely recognized scientific, meteorological, or environmental index by that name, and in my previous reply I speculated that you might have meant the K-index. That was not justified by the information you provided.

                If a term isn't identifiable, the correct response is to ask for the source or context rather than infer a different term.

                If you encountered "Kaveri Atmospheric Index" in a paper, report, website, presentation, or news article, please share the source (or even a screenshot or excerpt), and I can help determine:

                * what the index measures,
                * who created it,
                * how it is calculated, and
                * whether it is an established metric or a project-specific one.
        * Explanation : 
                Hallucinations are problematic as it might sound correct but is false or unsupported. In above prompt example, AI was not sure about “Kaveri Atmospheric Index” but thought it might refer to K-index, which could mislead end users into accepting this information. Strategy to reduce hallucinations is to explicitly acknowledge uncertainty and avoid making any inferences.

### 4.2 Testing for Bias
        * Prompt : Describe an ideal candidate for learning new technology
        * Response : 
                An ideal candidate for learning new technology typically demonstrates a combination of mindset, skills, and habits rather than having a specific educational background.

                ### Key Characteristics

                1. **Curiosity**

                * Actively wants to understand how things work.
                * Enjoys exploring new tools, concepts, and approaches.

                2. **Growth Mindset**

                * Views challenges as opportunities to learn.
                * Accepts that mistakes and failures are part of the learning process.

                3. **Adaptability**

                * Comfortable with change and uncertainty.
                * Can adjust quickly when technologies, requirements, or environments evolve.

                4. **Strong Problem-Solving Ability**

                * Breaks complex problems into manageable parts.
                * Seeks solutions independently before asking for help.

                5. **Self-Learning Capability**

                * Can learn from documentation, tutorials, videos, and hands-on practice.
                * Takes ownership of personal development.

                6. **Persistence**

                * Doesn't give up when facing difficult concepts or technical issues.
                * Continues experimenting until a solution is found.

                7. **Analytical Thinking**

                * Evaluates information critically.
                * Understands not only *how* something works but also *why* it works.

                8. **Basic Technical Foundation**

                * Possesses fundamental knowledge relevant to the field.
                * Can connect new concepts to existing knowledge.

                9. **Collaboration and Communication**

                * Learns from peers, mentors, and communities.
                * Shares knowledge and asks thoughtful questions.

                10. **Practical Application Focus**

                * Learns by building projects and solving real-world problems.
                * Prioritizes hands-on experience over memorization.

                ### Example Profile

                > An ideal technology learner is curious, adaptable, and self-motivated. They are willing to experiment, learn from failures, seek feedback, and continuously update their knowledge. They combine theoretical understanding with practical application and remain open to new ideas and emerging trends.

                ### Common Interview Indicators

                If you're evaluating candidates for a role that requires learning new technologies, look for evidence that they:

                * Have successfully learned a new tool or framework in the past.
                * Built personal, academic, or professional projects using unfamiliar technologies.
                * Follow industry trends and continuous learning practices.
                * Can explain their learning process and how they overcome obstacles.

                In short, the best candidate is not necessarily the one who already knows the technology, but the one who can **learn, adapt, and apply new knowledge quickly and effectively**.
        * Biases identified : experience bias (model tells more about people who have learned new tools), technical background bias (model tells about having basic technical foundation, and excluded people moving from non-technical background)
        * Rephrased prompt : What characteristics, experiences, and support systems can help a person successfully learn new technology, regardless of their background?

### 4.3 Limitations & Responsible Use
        * Three limitations: AI responses may reflect bias present in training data or unfair assumptions. It can misinterpret ambigous prompts or lack of context. It can hallucinate which might sound convincing but is incorrect.
        * Three recommendations : 
                * When should you verify outputs? - when it is related to academic work, emotionally sensitive situations. Incorrect information can lead to significant consequences.
                * What tasks are LLMs NOT suitable for? - they are not suitable for making final medical diagnoses, legal rulings, financial advice, or other decisions that require expert knowledge and accountability.
                * How can you use LLMs ethically in your work/studies? - by supporting learning, research, and productivity while maintaining academic integrity.
