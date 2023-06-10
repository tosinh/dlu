<script>
    import Header from "../components/header.svelte";
    import Nav from "../components/nav.svelte";
    import Carousel from "../components/carousel.svelte";
    import Admissions from "../components/admissions.svelte";
    import Content from "../components/content.svelte";
    import Partner from "../components/partner.svelte";
    import Studentdlu from "../components/studentdlu.svelte";
    import Footer from "../components/footer.svelte";

    const images = [
        {
            id: "a1",
            path: "../src/public/carousel/anh1.jpg",
        },
        {
            id: "a2",
            path: "../src/public/carousel/anh2.png",
        },
        {
            id: "a3",
            path: "../src/public/carousel/anh3.png",
        },
    ];
</script>

<svelte:head>
    <title>Trường đại học Đà Lạt</title>
</svelte:head>

<Header />
<Nav />
<Carousel
    {images}
    imageWhidth={980}
    imageSpacing={20}
    autoplay={true}
    autoplaySpeed={3000}
/>
<Admissions />
<Content />
<Partner />
<Studentdlu />
<Footer />
