cmake_minimum_required(VERSION 3.22)
project(HandlingMIDIEvents VERSION 0.01)

set(CMAKE_CXX_STANDARD 20)

add_subdirectory(libs/JUCE)
juce_add_gui_app(HandlingMIDIEvents PRODUCT_NAME "HandlingMIDIEvents")
target_link_libraries(HandlingMIDIEvents
        PRIVATE
            juce::juce_audio_basics
            juce::juce_audio_utils
    )
add_subdirectory(src)