import { useState } from "react";
import { useWindowEvent } from "./useWindowEvent";

export default function useWindowScroll() {
    const [scroll, setScroll] = useState({
        x: window?.scrollX,
        y: window?.scrollY,
    });
    useWindowEvent("scroll", () => {
        setScroll({ x: window?.scrollX, y: window?.scrollY });
    });

    function scrollTo(vector) {
        const { x, y } = { ...scroll, ...vector };
        window.scroll(x, y);
    }
    return [scroll, scrollTo];
}
