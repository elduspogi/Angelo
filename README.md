# Spring Security Authentication For My SamCho Crushie Angelo

    1.  > Go to security-for-angelo/src/main/resources/application.yml.
        > Change this:
            spring:
                datasource:
                #    Change the "payroll" to your Schema Name
                    url: jdbc:mysql://localhost:3306/payroll
                #    Change this to your db username
                    username: root
                #    Change this to your db password
                    password: localhost123
                    driver-class-name: com.mysql.cj.jdbc.Driver
    2.  > In your browser go to this url: https://generate-random.org/encryption-key-generator to generate your KEY
        > Go to security-for-angelo/src/main/java/config/JwtService.java and paste the generated key in this code:
            private static final String SECRET_KEY = "";
    3.  > Optional, you can change the Request Mapping in the DemoController.java and in the AuthenticationController.java. Making sure they are THE SAME.
            AuthenticationController.java:
                @RequestMapping("/angelo/spring/auth")
            DemoController.java:
                @RequestMapping("/angelo/spring/auth")
        > If you have made changes in the two java files, change also the SecurityConfiguration.java in this line of code:
            .requestMatchers("/angelo/spring/auth/**")
            Added the "/**" to apply the security configuration on all the url.




