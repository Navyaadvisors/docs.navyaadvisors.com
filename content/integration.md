This document serves as a comprehensive guide to integrating the **`NAVYA: Web Services`** into your system.

- [Getting Started](#getting-started)
- [Broker Hash](#broker-hash)
- [iframe Setup](#iframe-setup)
- [Example](#example)

## Getting Started

This requires no extra installation of plugin or SDK as long as you can incorporate our portal into your web application using an iframe.

!!! tip
    You need to acquire a broker hash for integration

## Broker Hash

The brokers will be provided with a unique broker hash for integration of NAVYA: Web Services in their website.

This broker hash will be passed to the source URL of the iframe where the service will be accessed.

Please use the below provided test hash for testing the integration

!!! info "Test Hash for sandbox environment"

    > **Test Hash:**
    342d05d0-0e01-11ef-a7c3-df9aa7a55d7f

## iframe Setup

Since **`NAVYA: Web Services`** is a web-based service, the broker will integrate our service into their website through iframes.

iframes are html tags which helps to open/access external website inside a webpage. For integration of **`NAVYA: Web Services`** into the broker page, the webpage/website must use the following parameters in their iframe tag.

!!! info "Parameters"
    - **loading** = "lazy"
    - **referrerPolicy** = "strict-origin-when-cross-origin"
    - **sandbox** = "allow-same-origin allow-scripts allow-popups allow-forms allow-top-navigation"
    - **allow** = "accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    - **allowFullScreen**
    - **src** = "https://navyaadvisors.com/broker?id=**{broker_hash}**"

!!! warning "Note"
    The above-mentioned parameters are must have parameters. Additional parameters such as id, class or any styling parameters can be used as per broker’s discretion.

The concerned **source URL** which provides access to the service is:

!!! info "Source URL"
    **URL:** https://navyaadvisors.com/broker?id=***{broker_hash}***
    > **{broker_hash}:** The hash provided to the broker <br>
    > **Example:** https://navyaadvisors.com/broker?id=342d05d0-0e01-11ef-a7c3-df9aa7a55d7f

Here, brokers have to use the provided **broker hash** in the **‘{broker_hash}’** portion of the above-mentioned URL.

!!! example "For example, using the test broker hash, the source URL becomes:" 
    >**URL:**
    *https://navyaadvisors.com/broker?id=342d05d0-0e01-11ef-a7c3-df9aa7a55d7f*

## Example

!!! example "Example Snippet"
    ```html
    <iframe
        loading="lazy"
        src="https://navyaadvisors.com/broker?id=342d05d0-0e01-11ef-a7c3-df9aa7a55d7f"
        referrerPolicy="strict-origin-when-cross-origin"
        sandbox="allow-same-origin allow-scripts allow-popups allow-forms allow-top-navigation"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowFullScreen
    ></iframe>
    ```
